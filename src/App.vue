<template>
  <div class="app-wrapper">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="josh mu is using Vue" /> -->
    <Header />
    <div class="main-wrapper">
      <Sidebar />
      <Content />
    </div>
    <Footer />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import Content from './components/Content.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Header,
    Sidebar,
    Content,
    Footer,
  },
}
</script>

<style lang="scss" scoped>
@import './styles/variables.scss';

.app-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: start;

  .main-wrapper {
    display: flex;
    flex: 1;
    width: 100%;
    min-height: calc(100vh - #{($header-height + $footer-height)});
  }
}
</style>
