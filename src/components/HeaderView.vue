<template>
  <header id="header" class="header">
    <h3 class="logo"><a href="/">Mohammad Ayash</a></h3>
    <div class="header-menu d-print-none">
      <div class="logo-img"></div>
      <ul class="nav nav-tabs ">
        <li class="nav-item">
          <router-link to="/" class="nav-link">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" class="nav-link">about</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/weather" class="nav-link">weather</router-link>
        </li>
      </ul>
    </div>
  </header>
</template>
<script>
</script>
<style>
header {
  background-color: #f0f0f0;
  width: 100%;
  position: fixed;
  z-index: 5;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
}

header .logo a {
  text-decoration: none;
  text-align: center;
}
@media print {
  header {
    background-color: rgb(57, 90, 135);
  }
  header .logo a {
    color: rgb(57, 90, 135);
  }
}@media (max-width: 480px){
  header{
    flex-direction: column;
    width: 100%;   
  }

  
}
</style>