<template>
  <section class="contact" id="contact">
    <div class="contact-content m-2">
      <h2 class="contact-title">Contact me with</h2>
      <div class="icon">
        <i class="fas fa-envelope"></i>
      </div>
      <div class="info">
        <h3>Email:</h3>
        <p>Mohammadhd1987@gmail.com</p>
      </div>
    </div>
  </section>
</template>
<script>
export default {};
</script>
<style>
.contact {
  font-weight: bold;
  background-color: rgba(245, 244, 237, 0.358);
  min-height: 100vh;
  margin-top: -10px;
}
.contact-title {
  width: 25%;
  margin: 20px;
  padding: 20px 0px;
  background-color: rgb(4, 4, 75);
  font-size: large;
  font-weight: bold;
  color: rgb(237, 239, 245);
  text-align: center;
  border-radius: 5%;
}
.contact-content {
  margin: 20px;
}
.contact .icon {
  color: rgb(35, 67, 227);
  font-size: 4.5em;
}
.contact .info h3 {
  display: inline-block;
  color: rgb(1, 5, 51);
}

 .info p {
  font-size: 1.5em;
  padding: 10px;
}
@media (max-width: 768px) {
  .contact {
    text-align: center;
  }
  .info p{
    font-size: 2em;
    padding: 2px;
  }
  
}
@media (max-width: 576px) {
  .contact-title{
    width: 90%;
  }
  .info p{
    font-size: 1.3em;
    padding: 2px;
  }
}
</style>
