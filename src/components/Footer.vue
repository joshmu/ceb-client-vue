<template>
  <div class="footer">
    <p>Footer</p>
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

.footer {
  max-width: $breakpoint-lg;
  height: $footer-height;
  align-self: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
