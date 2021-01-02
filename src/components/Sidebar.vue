<template>
  <div class="sidebar-wrapper">
    <div class="sidebar">
      <nav class="sidebar__nav">
        <ul>
          <li>Overview</li>
          <li>Bitcoin</li>
          <li>Ethereum</li>
          <li>Tether</li>
        </ul>
      </nav>
    </div>
  </div>
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

.sidebar-wrapper {
  display: flex;
  justify-content: start;
  align-items: start;

  .sidebar {
    border-right: 1px solid rgba(255, 255, 255, 0.5);
    margin-right: 2rem;
    padding: 2rem 0;

    .sidebar__nav {
      font-size: 1.25rem;
      font-style: italic;
      text-align: right;

      ul {
        li {
          padding: 0.25rem 1.25rem;
          cursor: pointer;
          @include hover-flip;
        }
      }
    }
  }
}
</style>
