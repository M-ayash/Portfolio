<template>
  <nav id="nav-menu" class="nav-menu">
    <div class="header-menu d-print-none">
      <ul class="nav nav-tabs justify-content-end">
        <li class="nav-item">
          <router-link to="/projects" class="nav-link">Projects</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" class="nav-link">About</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/contact" class="nav-link">Contact</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/weather" class="nav-link">Weather</router-link>
        </li>
      </ul>
    </div>
  </nav>
</template>
<style>
  .nav-tabs {
    border: none !important;
  }
  .nav-tabs .nav-link,
  .nav-tabs .nav-link {
    border: none !important;
  }
  .nav-tabs .nav-link:hover,
  .nav-tabs .nav-link:focus {
    border: none;
  }
  .nav-tabs li a {
    color: #fff;
  }
</style>
<script></script>
