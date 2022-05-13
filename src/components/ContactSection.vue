<template>
  <section class="contact" id="contact">
    <div class="content m-2">
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
  text-shadow: 5px 5px 10px #eef7ee;
  background-color: rgb(101, 157, 243);
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
  color: #000;
}

.contact .info p {
  font-size: 1.5em;
}
@media (max-width: 768px) {
  .contact {
    text-align: center;
  }
}
</style>
