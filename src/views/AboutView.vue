<template>
  <div class="about">
    <CurriculumVitae/>
  </div>
</template>
<script>
import CurriculumVitae from "../components/CurriculumVitae.vue";

export default {
    components: { CurriculumVitae }
}
</script>
<style>
.about{
  padding-top: 10px;
}
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
