<script>
import FooterView from "./components/FooterView.vue";
import HeaderView from "./components/HeaderView.vue";
export default {
  components: { HeaderView, FooterView },
};
</script>
<template>
  <div>
    <header-view />
    <div class="main">
      <router-view />
    </div>
    
    <footer-view />
  </div>
</template>
<style>
#app {
  box-sizing: border-box;
  font-family: 'Times New Roman', Times, sans-serif;
  scroll-behavior: smooth;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
.main{
  padding: 0;
  margin: 0;
  padding-top: 4.5em;
}
@media (max-width: 810px) {
  #app {
    font-family:Arial, Helvetica, sans-serif;
  
  }
}
  @media (max-width: 360px) {
  #app {
    font: 0.5em sans-serif;
  }
  
}
</style>
