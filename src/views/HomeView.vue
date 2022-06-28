<template>
  <div class="home">
    <img src="@/assets/img/sky8.jpg" alt="" class="background-img" />
    
    <div class="moon-img">
      <img src="../assets/img/moon1.png" alt="moon" class="rounded-circle" />
    </div>

    
    <div id="star0" class="star"></div>
    <MainPage />
    <ExperienceSection />
    <ContactSection />
  </div>
</template>
<script>
import ExperienceSection from "../components/ExperienceSection.vue";
import ContactSection from "../components/ContactSection.vue";
import MainPage from "../components/MainPage.vue";
export default {
  name: "Home",
  components: { ExperienceSection, ContactSection, MainPage },
  methods: {
    addStar(n) {
      let star = document.getElementById("star0");
      for (let i = 0; i < n; i++) {
        let st = star.cloneNode(true);
        st.style.top = `${Math.floor(Math.random() * 100)}px`;
      }
    },
  },
};
</script>
<style>
.home {
  position: relative;
  /*background: url("@/assets/img/sky8.jpg");*/
  background-size: cover;
  background-position: sticky;
  background-attachment: fixed;
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