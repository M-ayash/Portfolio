<template>
  <header id="header" class="header">
    <a class="logo" href="/"><h3>Mohammad Ayash</h3></a>
    <div class="header-menu d-print-none">
      <div class="logo-img"></div>
      <ul class="nav nav-tabs justify-content-end">
        <li class="nav-item">
          <router-link to="/" class="nav-link">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" class="nav-link">About</router-link>
        </li>
      </ul>
    </div>
  </header>
</template>
<script></script>
<style>
header {
  min-height: 4em;
  background-color: #100f0f;
  width: 100%;
  position: fixed;
  z-index: 5;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
}
.logo {
  text-decoration: none;
}
.logo h3 {
  text-transform: uppercase;
  font: bold 2em Open Sans, Impact;
  text-align: center;
  line-height: 1.5em;
  display: table;
  color: rgb(243, 243, 247);
  -webkit-text-stroke: 1px rgb(57, 90, 135);
}
.logo:hover h3 {
  color: rgb(96, 152, 231);
}
.nav-item a {
  color: #81a9b5;
  font-weight: bold;
}
.nav-item:hover {
  transform: translateY(-10%);
}
@media print {
  header {
    background-color: rgb(57, 90, 135);
  }
  header .logo h3 {
    color: rgb(57, 90, 135);
  }
}
</style>
