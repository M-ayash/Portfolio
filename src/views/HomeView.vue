<template>
  <div class="home">
    <div id="star0" class="star">
    </div>
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
    components: { ExperienceSection, ContactSection, MainPage },
    methods: {
      addStar(n){
       let star= document.getElementById('star0')
        for(let i=0;i<n;i++){
            let st=star.cloneNode(true)
            st.style.top=`${Math.floor(Math.random()*100)}px`
        }
      }
    },
}
</script>
<style>
.home{
  background: url("@/assets/img/sky8.jpg");
  background-size: cover;
  background-position: sticky;
  background-attachment: fixed;
  background-color: blue;
  }
  .star{
    position: absolute;
    top: 200px;
    left: 10%;
    width: 10px;
    height: 10px;
    border-radius: 50%;
   background-color:  #8ad9ea;
   box-shadow:2px 2px #8ad9ea;
   filter: blur(1px);
   animation: bright 5s linear 2s infinite alternate;
  }
  @keyframes bright {
    from{
      filter: blur(1px);

    }
    to{
      filter: blur(7px);
    }
  }

</style>