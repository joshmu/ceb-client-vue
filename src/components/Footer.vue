<template>
  <div class="footer">
    <p class="copyright">
      <a class="mu-dev" href="https://joshmu.dev" target="_blank"
        >MU - {{ currentYear }}</a
      >
    </p>
  </div>
</template>
<script>
export default {
  setup() {
    const currentYear = new Date().getFullYear()

    return {
      currentYear,
    }
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

  .copyright {
    $opacity: 0.75;
    letter-spacing: 3px;
    font-size: 0.5rem;
    padding: 0.5rem 1rem;
    opacity: $opacity;
    @include hover-underline($opacity);
  }
}
</style>
