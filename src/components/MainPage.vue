<template>
  <section class="main-page pt-3" id="main-page">
    <ul class="nav justify-content-end">
      <li class="nav-item">
        <button @click="goto('my-skills')" class="btn btn-light me-4">
          My Skills
        </button>
      </li>
      <li class="nav-item">
        <button @click="goto('contact')" class=" btn btn-contact me-4">
          Contact
        </button>
      </li>
    </ul>
    <div class="main-content">
      <div class="main-parg">
        <h5>Hello I am</h5>
        <h1>Mohammad</h1>
        <h3>Front-end Developer</h3>
        <p>
          I am a web developer with frontend experience Knowledge of HTML, CSS,
          Javascript Wordpress and Vuejs.
        </p>
        <div class="social-icons">
          <a
            class="fa-brands fa-twitter"
            href="https://twitter.com/Mohammad_ay_87"
          ></a>
          <a
            class="fa-brands fa-facebook"
            href="https://www.facebook.com/mohammad.ayash.88"
          ></a>
          <a
            class="fa-brands fa-linkedin"
            href="https://www.linkedin.com/in/mohammad-ayash-465216231/"
          ></a>
          <a
            class="fa-brands fa-instagram"
            href="https://www.instagram.com/mohammad.ayash.88/"
          ></a>
          <a class="fa-brands fa-github" href="https://github.com/M-ayash"></a>
        </div>
        <div>
          <a class="btn btn-contact m-4" @click="goto('contact')"
            >Contact</a
          >
        </div>
      </div>
      <div class="main-img">
        <img
          src="../assets/img/moon1.png"
          alt="laptop"
          class="rounded-circle"
        />
      </div>
      <div>
        <button
          class="btn text-white border border-white btn-scroll-top"
          @click="goto('main-page')"
          title="go top"
        >
          &#8679;
        </button>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  methods: {
    goto(id) {
      var element = document.getElementById(id);
      element.scrollIntoView({
        behavior: "smooth",
      });
    },
  },
};
</script>
<style>
.main-page {
  min-height: 100vh;
  min-width: 100%;
}
.main-content {
  display: flex;
  min-height: 90vh;
  min-width: 100%;
  align-items: center;
  justify-content: space-evenly;

}
.main-parg {
  float: left;
  width: 40%;
  font-weight: bold;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
.main-parg h1 {
  font-size: 100px;
  color: rgb(151 204 237);
  animation: nameStart 2s linear 0s normal;
}
@keyframes nameStart {
  0% {
    transform: translate(0px, -400px);
  }
  80% {
    transform: translate(0px, -400px);
  }
  90% {
    transform: translate(0px, 40px);
  }
}
.main-parg h3 {
  font-size: 50px;
  color: rgb(31, 169, 207);
}
.main-parg h5 {
  font-size: 40px;
  color: #03242e;
  text-shadow: -1px 0 rgb(248, 244, 244), 0 1px rgb(245, 243, 243),
    1px 0 rgb(248, 244, 244), 0 -1px rgb(245, 240, 240);
}
.main-parg p {
  font-size: 25px;
  justify-content: center;
  color: coral;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
.social-icons a {
  padding: 10px;
  text-decoration: none;
  font-size: 20px;
  color: #f7f7f7;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
.btn-contact {
  font-size: 20px;
  padding: 20px 50px;
  background-color: #81a9b5!important;
  color: #fff !important;
}
.btn-scroll-top {
  position: fixed;
  padding: 20px;
  bottom: 5px;
  right: 5px;
  border-radius: 10px;
}
.main-img {
}
.main-img img:hover {

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
@media (max-width: 768px) {
  .main-page {
    margin: 5px;
    padding: 10px;
    flex-direction: column;
  }
  .main-content {
    display: block;
    flex-direction: column;
  }
  .main-parg {
    width: 100%;
    text-shadow: 1px solid black;
    padding: 0;

  }
  .main-parg h1 {
    font-size: 4em;
  }
  .main-parg h3 {
    font-size: 3em;
  }
  .main-parg h5 {
    font-size: 1.5em;
  }
  .main-parg p {
    font-size: 1.5em;
  }
  .btn-contact {
    font-size: 20px;
  }
  .main-img {
    text-align: center;
  }
  @media (max-width: 576px) {
    .main-page {
      padding: 20px;
      padding-top: 6em;
    }
  }
}
</style>