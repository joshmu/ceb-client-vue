<template>
  <header class="header">
    <div class="logo">
      <a href="#"><h1>CEB</h1></a>
    </div>
    <ul class="menu">
      <li class="menu-item">About</li>
      <li class="menu-item"><a href="mailto:mu@joshmu.com">Contact</a></li>
    </ul>
  </header>
</template>

<script>
export default {
  setup() {
    return {}
  },
}
</script>

<style lang="scss" scoped>
@import '../styles/variables.scss';

.header {
  max-width: $breakpoint-lg;
  height: $header-height;
  width: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;

  .menu {
    display: flex;
    list-style: none;
    text-transform: uppercase;
    letter-spacing: 1px;

    .menu-item {
      $underline-opacity: 1;
      padding: 0.5rem 1rem;
      @include hover-underline($underline-opacity);
    }
  }
}
</style>
