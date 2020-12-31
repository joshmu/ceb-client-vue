<template>
  <header class="header">
    <div class="logo"><h1>CEB</h1></div>
    <ul class="menu">
      <li class="menu-item">About</li>
      <li class="menu-item">Contact</li>
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
    gap: 1rem;

    .menu-item {
      position: relative;
      cursor: pointer;
      &:after {
        content: '';
        position: absolute;
        height: 1px;
        background-color: white;
        width: 0%;
        bottom: 0;
        left: 0;
        transition: opacity, width 0.3s ease-in-out;
        opacity: 0;
      }
      &:hover {
        &:after {
          opacity: 1;
          width: 100%;
        }
      }
    }
  }
}
</style>
