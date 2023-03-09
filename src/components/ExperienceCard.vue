<template>
  <div class="experience-card">
    <div class="experience-image">
      <slot></slot>
    </div>
    <div class="experience-info">
      <p class="experience-category">{{ cardText }}</p>
    </div>
    <div class="experience-footer">
      <i class="fa-solid fa-power-off"></i>
    </div>
  </div>
</template>
<script>
  export default {
    props: ["cardText"],

    methods: {},
  };
</script>
<style>
  .experience-card {
    position: relative;
    background-color: rgba(246, 245, 237, 0.947);
    border: 15px solid #000;
    border-bottom-width: 20px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    width: 28%;
    max-height: 260px;
    margin: 1em;
    padding: 1em 1em 7em 1em;
    cursor: pointer;
  }
 .experience-card:hover .experience-footer {
   color: #56ff13;
   
  }
  .experience-card:hover img{
    transform: scale(1.1);
    
  }
  .experience-card a {
    text-decoration: none;
  }

  .experience-card:hover .experience-image {
    opacity: 0.9;
  }
  .experience-image {
    max-height: 75%;
  }
  .experience-image img {
    width: 100%;
    height: 170px;
    border-radius: 5%;
    pointer-events: none;
  }
  .experience-info {
    position: absolute;
    bottom: -10px;
    display: block;
    left: 0;
    width: 100%;
  }
  .experience-category {
    font-size: 20px;
    color: #0c1eb3;
    /* text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black; */
    text-align: center;
    padding-top: 10px;
  }
  .experience-category small {
    display: block;
    font-size: 15px;
  }
  .experience-footer {
    position: absolute;
    bottom: -22px;
    left: 49%;
    color: #ff2929;
  }
  @media (max-width: 1200px) {
    .experience-card {
      max-width: none;
      width: 45%;
    }
  }
  @media (max-width: 768px) {

  }
  @media (max-width: 576px) {
    .experience-card {
      width: 90%;
    }
    .experience-category {
      font-size: 0.9em;
    }
    .experience-footer {
      bottom: -16px;
    }

  }
</style>
