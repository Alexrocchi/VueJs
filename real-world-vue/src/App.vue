<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="alert alert--dark">
    <span>&#128679; Under construction &#128679;</span>
  </div>
  <div id="layout">
    <header>
      <div class="wrapper">
        <nav>
          <RouterLink to="/">Events</RouterLink> |
          <RouterLink to="/about">About</RouterLink>
        </nav>
      </div>
    </header>
    <RouterView />
  </div>
</template>

<style>
  #layout {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  nav {
    padding: 30px;
  }
  nav a {
    font-weight: bold;
    color: #2c3e50;
  }
  nav a.router-link-exact-active {
    color: #42b983;
  }
  h2 {
    font-size: 20px;
  }
  body{
    margin: 0 auto;
  }
  .alert{
    text-align: center;
    padding: 8px;
    width: 100%;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold;
  }
  .alert--dark{
    background-color: #212529;
    color: #fff;
  }
</style>
