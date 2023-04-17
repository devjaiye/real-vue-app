<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
<div id="layout">
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink :to="{name: 'event-list'}">Event</RouterLink> |
        <RouterLink :to="{name: 'about'}">About</RouterLink>
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
h2{
  color: red;
  font-size: 18px;
}
</style>


<!-- For your final coding challenge:

Add a question to the review-form: 'Would you recommend this product? ’

Record and emit the response, and display it within review-list

As a reminder, if you’re coding along with our repo, you can check out L11-end branch. -->