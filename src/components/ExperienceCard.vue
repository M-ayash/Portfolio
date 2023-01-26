<template>
  <div class="experience-card">
      <div class="experience-image">
        <slot></slot>
      </div>
      <div class="experience-info">
        <p class="experience-category">{{ cardText }}</p>
      </div>
    </div>
</template>
<script>
export default {
  props: ["cardText"],
  
  methods:{
   
  }
};
</script>
<style>
.experience-card {
  position: relative;
  background-color: rgba(246, 245, 237, 0.947);
  border: 15px solid #000;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  max-width: 28%;
  margin: 1em;
  padding: 1em 1em 7em 1em;
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

.experience-image img {
  width: 100%;
  border-radius: 10%;
}
.experience-info{
  position: absolute;
  bottom: 10px;
  display: block;
  left: 0;
  width: 100%;
}
.experience-category {
  font-size: 20px;
  color: #000;
  /* text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black; */
  text-align: center;
  padding-top: 10px;

}
.experience-category small {
  display: block;
  font-size: 15px;
}
@media (max-width: 768px) {
  .experience-card{
    max-width: 30%;
  }

  
}
@media (max-width: 576px) {
  .experience-card{
    max-width:none;
  }
  .experience-category {
    font-size: 0.7em;
    
  }
}
</style>
