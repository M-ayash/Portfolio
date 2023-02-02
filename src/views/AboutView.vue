<template>
  <div class="about">
    <div class="about-main">
      
      <div v-if="!show">
        <div class="page-title">
        <h1><span></span>About me</h1>
      </div>
        <h2>Over mij</h2>
        <p>
          Als front-end developer ben ik verantwoordelijk voor het design en de
          implementatie van user interfaces binnen webapplicaties om te komen
          tot het beste resultaat dat klanten tevreden stelt . IK ontwerp mooie
          moderne dynamische websites met HTML CSS JavaScript VueJs and
          WordPress .
        </p>
      </div>
      <div class="close-cv">
        <button
        type="button"
        class="btn hidden-cv"
        :class="{ 'show-cv': show }"
        @click="show = !show"
      >
        {{ show ? "&#9747;" : "Mijn CV" }}
      </button>
      </div>
      
    </div>
    <!-- <img src="../assets/img/sky4.jpg" alt="" class="about-bg" /> -->
    <CurriculumVitae v-if="show" />
  </div>
</template>
<script>
import CurriculumVitae from "../components/CurriculumVitae.vue";

export default {
  components: { CurriculumVitae },
  name: "about",
  data() {
    return {
      show: false,
    };
  },
};
</script>
<style>
.about {
  display: flex;
  position: relative;
  min-height: 100vh;
  padding-top: 10px;
}
.about-main {
  position: relative;
  width: 70%;
  color: #fff;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
.about-main h2 {
  color: rgb(12, 135, 235);
  padding: 20px;
}
.about-main p {
  font-size: 1.4em;
   text-align: justify;
   padding: 20px;
}
.hidden-cv {
  background-color: rgb(9, 151, 187);
  margin: 20px;
}
.show-cv {
  position: fixed;
  top: 20%;
  left: 70%;
  background-color: #0c010115;
}
.about-bg {
  position: fixed;
  width: 100%;
  height: 100%;
  z-index: -100;
}

@media (max-width: 768px) {
  .about-main {
    padding-top:10em;
    width: 100%;
  }
  .show-cv{
    top: 20%;
  left: 80%;
  }
  @media print {
    .close-cv{
      display: none !important;
      visibility: hidden;
    }
    .close-cv .hidden-cv{
      visibility: hidden;
    }
    .show-cv{
      background-color: transparent;
    }
  }
}
</style>
