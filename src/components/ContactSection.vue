<template>
  <section class="contact" id="contact">
    <div class="page-title">
        <h1><span></span>Contact</h1>
    </div>
    <div class="contact-content ">
      <h2 class="contact-title">Contact me with</h2>
      <div class="icon">
        <i class="fas fa-envelope"></i>
      </div>
      <div class="info">
        <h3>Email:</h3>
        <p><a href="mailto:Mohammadhd1987@gmail.com">Mohammadhd1987@gmail.com</a> </p>
      </div>
      <div class="contact-content-footer">
      <i class="fa-solid fa-power-off"></i>
    </div>
    </div>
  </section>
</template>
<script>
export default {
};
</script>
<style>
.contact {
  font-weight: bold;
  min-height: 100vh;
  margin-top: -10px;
  
}
.contact-title {
  margin: 20px;
  padding: 20px 0px;
  font-size: 2em;
  font-weight: bold;
 
  text-align: center;
  border-radius: 5%;
}
.contact-content {
  background-color: rgba(246, 245, 237, 0.947);
    border: 15px solid #000;
    border-bottom-width: 20px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    padding: 10px;
    width: 50%;
    position: relative;
    margin: auto;
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
.contact-content-footer {
    position: absolute;
    bottom: -19px;
    left: 49%;
    color: #f7f4f4;
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
