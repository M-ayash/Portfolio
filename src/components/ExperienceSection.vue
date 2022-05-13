<template>
  <section class="experience" id="my-skills" ref="my-skills">
    <div class="experience-title"><span>My skills</span></div>

    <div class="row experience-content">
      <div class="col-2 experience-card">
        <div class="experience-image">
          <img src="@/assets/img/html_img.png" />
        </div>
        <div class="experience-info">
          <p class="experience-category">HTML</p>
        </div>
      </div>
      <div class="col-2 experience-card">
        <div class="experience-image">
          <img src="@/assets/img/css_img.png" />
        </div>
        <div class="experience-info">
          <p class="experience-category">CSS</p>
        </div>
      </div>
      <div class="col-2 experience-card">
        <div class="experience-image">
          <img src="@/assets/img/js-img.png" />
        </div>
        <div class="experience-info">
          <p class="experience-category">Javascript</p>
        </div>
      </div>
      <div class="col-2 experience-card">
        <div class="experience-image">
          <img src="@/assets/img/vuejs_img.png" />
        </div>
        <div class="experience-info">
          <p class="experience-category">Vuejs</p>
        </div>
      </div>
      <div class="col-2 experience-card">
        <div class="experience-image">
          <img src="@/assets/img/wp_img.png" />
        </div>
        <div class="experience-info">
          <p class="experience-category">Wordpress</p>
        </div>
      </div>
      <div class="col-2 experience-card">
        <iframe src="" frameborder="0"></iframe>
      </div>
    </div>
  </section>
</template>

<script>

export default {
    components: { }
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
}
.experience-card:hover {
  transform: scale(1.1);
}

.experience-card:hover .experience-image {
  opacity: 0.9;
}

.experience-image img {
  width: 100%;
}
.experience-category {
  font-size: 20px;
  color: coral;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
  text-align: center;
}
@media (max-width: 400px) {
  .experience-category{
    font-size: 0.7em;
  }
}
</style>