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
  background-color: rgba(244, 243, 223, 0.548);
  max-width: 21%;
  margin: 1em;
  padding: 1em;
  cursor: pointer;
  border-radius: 10%;
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
