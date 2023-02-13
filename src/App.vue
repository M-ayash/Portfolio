<script>
import FooterView from "./components/FooterView.vue";
import HeaderView from "./components/HeaderView.vue";
import NavMenu from "./components/NavMenu.vue";
export default {
  components: { HeaderView, FooterView, NavMenu },

};


</script>
<template>
  <div>
    <header-view />
    <div class="main">
      <div class="container">
        <navMenu />
        <router-view />
      </div>  
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
  padding: 8.5em 0;
  width: 100%;
  margin: 0;
  background-image: radial-gradient(
    farthest-corner,
    #12d2e4,
    #0929ca,
    #3f3f5d,
    #303040,
    #333334
  );
}
.main .container{
  width: 75%;
  margin: 0 0 0 20px;
  border: 4px solid #000;
  border-radius: 20px;
  background-image: radial-gradient(
    farthest-corner,
    #1e7a83,
    #1a286f,
    #383855,
    #292935,
    #232323
  );
  padding-bottom: 4em;
  position: relative;
}
.page-title {
  padding: 2em 0;
  font-weight: bold;
  text-align: center;
  margin-bottom: 50px;
  /* text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;*/
}
.page-title h1 {
  font-size: 5em;
  font-weight: bold;
  color: #fff;
}
.page-title h1 span {
  display: inline-block;
  padding: 6px 55px 0 0;
  transform: rotate(-60deg);
  background: linear-gradient(
    to right,
    #ee05ffb6,
    #ff0066e2,
    rgba(254, 1, 1, 0.811)
  );
  margin-bottom: 23px;
}
.page-title h1::before {
  content: "\003C";
  color: #1c1919;
}
.page-title h1::after {
  content: "\003E";
  color: #1c1919;
}
.page-title p {
  font-size: 1.2em;
  margin: 0 auto;
  color: #41dd16;
  width: 50%;
}
@media (max-width: 810px) {
  #app {
    font-family:Arial, Helvetica, sans-serif;
  
  }
  .main .container{
    width: 90%;
  }
  .page-title {
    width: 100%;
    text-shadow: 1px solid black;
    padding: 0;
  }
  .page-title h1 {
    font-size: 2.5em;
  }
  .page-title h3 {
    font-size: 2.8em;
  }
  .page-title h5 {
    font-size: 1.5em;
  }
  .page-title p {
    font-size: 1.5em;
  }
  .page-title h1 span {
    padding: 5px 33px 0 0;
    margin-bottom: 8px;
  }
}

  @media (max-width: 480px) {
  #app {
    font: 0.5em sans-serif;
  }
  .page-title{
    margin-top: 20px;
  }
  .page-title h1 span {
    padding: 3px 17px 0 0;
    margin-bottom: 3px;
  }
  .main .container{
    margin: 24px 0px;
    width: 100%;
  }
}
@media print {
  #app{
    height: 100vh;
    background-color: #fff;
  }
  .main,.main .container{
    background: #fff;
    border: none;
    width: 100%;
    margin-bottom: 20px;
  }
}
</style>
