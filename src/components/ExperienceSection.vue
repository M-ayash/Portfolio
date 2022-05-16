<template>
  <section class="experience" id="my-skills" ref="my-skills">
    <div class="experience-title"><span>My skills</span></div>

    <div class="row experience-content">
      <div class="col-2 experience-card">
        <a href="https://moutaz-bakier.github.io/">
          <div class="experience-image">
            <img src="@/assets/img/form_builder.jpg" />
          </div>
          <div class="experience-info">
            <p class="experience-category">Form Builder</p>
          </div>
        </a>
      </div>
      <div class="col-2 experience-card" @click="this.$router.push('/about')">
        <div class="experience-image">
          <img src="@/assets/img/cv_with_CSS.jpg" />
        </div>
        <div class="experience-info">
          <p class="experience-category">CV with Html en CSS</p>
        </div>
      </div>
      <div class="col-2 experience-card" @click="this.$router.push('/weather')">
        <div class="experience-image">
          <img src="@/assets/img/weatherApp.jpg" />
        </div>
        <div class="experience-info">
          <p class="experience-category">weather App</p>
        </div>
      </div>
      <div class="col-2 experience-card">
        <a href="https://github.com/M-ayash/portfolio">
          <div class="experience-image">
            <img src="@/assets/img/portolio_wit_Vuejs.jpg" />
          </div>
          <div class="experience-info">
            <p class="experience-category">
              portfolio met Vuejs <small>(link to github)</small>
            </p>
          </div>
        </a>
      </div>
      <div class="col-2 experience-card">
        <div class="experience-image">
          <img src="@/assets/img/wp_img.png" />
        </div>
        <div class="experience-info">
          <p class="experience-category">Wordpress theme from scratch</p>
        </div>
      </div>
      <div class="col-2 experience-card">
        <div class="experience-info">
          <p class="experience-category">coming soon...</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  components: {},
};
</script>
<style>
.experience {
  min-height: 90vh;
  height: 100%;
  padding-top: 100px;
}
.experience-title {
  margin: 20px;
}
.experience-title span {
  padding: 10px 100px;
  background-color: rgb(4, 4, 75);
  font-size: large;
  font-weight: bold;
  color: rgb(237, 239, 245);
}
.experience-card {
  background-color: rgb(101, 157, 243);
  border: 1px solid rgb(18, 17, 17);
  border-radius: 10px;
  margin: 20px 40px;
  box-shadow: 5px 5px 5px 5px rgb(242, 245, 247);
  cursor: pointer;
}
.experience-card:hover {
  transform: scale(1.1);
}
.experience-card a {
  text-decoration: none;
}

.experience-card:hover .experience-image {
  opacity: 0.9;
}

.experience-image img{
  width: 100%;
}
.experience-category {
  font-size: 20px;
  color: coral;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
  text-align: center;
}
.experience-category small {
  display: block;
  font-size: 15px;
}
@media (max-width: 400px) {
  .experience-category {
    font-size: 0.7em;
  }
}
</style>