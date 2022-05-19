<template>
<div>
  <HeaderView />
  <MainView />
  <FooterView />
</div>
 
</template>
<script>
import { RouterLink, RouterView } from 'vue-router'
import MainView from './components/MainView.vue'
import FooterView from './components/FooterView.vue'
import HeaderView from './components/HeaderView.vue'
export default {
    components: { MainView, FooterView, HeaderView }
}
</script>
<style>
body {
  box-sizing: border-box;
  }
#app {
  font-family: 'Times New Roman', Times, sans-serif;
  scroll-behavior: smooth;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
@media (max-width: 810px) {
  #app {
    font-family:Arial, Helvetica, sans-serif;
  }
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(209, 91%, 45%, 0.2);
  }
}
</style>
