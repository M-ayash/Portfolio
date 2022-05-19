<template>
  <div class="home">
    <MainPage/>
    <ExperienceSection/>
    <ContactSection/>
  </div>
</template>
<script>
import ExperienceSection from "../components/ExperienceSection.vue";
import ContactSection from "../components/ContactSection.vue";
import MainPage from "../components/MainPage.vue";
export default {
    name: "Home",
    components: { ExperienceSection, ContactSection, MainPage }
}
</script>
<style>
.home{
  background: url("@/assets/img/img_3.jpg");
  background-size: cover;
  background-position: sticky;
  background-attachment: fixed;
  }

</style>