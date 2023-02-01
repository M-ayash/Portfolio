<template>
    <MainPage />
</template>
<script>
import ExperienceSection from "../components/ExperienceSection.vue";
import ContactSection from "../components/ContactSection.vue";
import MainPage from "../components/MainPage.vue";
export default {
  name: "Home",
  components: { ExperienceSection, ContactSection, MainPage },
  methods: {
  },
};
</script>
<style>
.home {
  position: relative;
 
}
.background-img {
  position: fixed;
  min-width: 100%;
  min-height: 100%;
  z-index: -100;
}
.moon-img img {
  position: absolute;
  top: 150px;
  right: 50px;
  width: 10%;
}


.moon-img img:hover {
  animation: rotation 40s linear 0s infinite forwards;
}
@keyframes rotation {
  form {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(-360deg);
  }
}
.star {
  position: sticky;
  top: 200px;
  left: 10%;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #8ad9ea;
  box-shadow: 2px 2px #8ad9ea;
  filter: blur(1px);
  animation: bright 5s linear 2s infinite alternate;
}
@keyframes bright {
  from {
    filter: blur(1px);
  }
  to {
    filter: blur(7px);
  }
}
</style>