<template>
  <main class="main">
    <router-view />
  </main>
</template>
<script>
import ContactSection from "./ContactSection.vue";
import ExperienceSection from "./ExperienceSection.vue";
export default {
  components: { ContactSection, ExperienceSection },
};
</script>

<style>
</style>
