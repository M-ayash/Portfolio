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
  overflow: auto;
}
.main{
  padding: 0;
  margin: 0;
  padding-top: 4.5em;
  background-image: radial-gradient(
    farthest-corner,
    #12d2e4,
    #0929ca,
    #3f3f5d,
    #303040,
    #333334
  );
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
