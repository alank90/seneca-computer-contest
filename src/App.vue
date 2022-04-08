<template>
  <TheNavigation />
  <div class="wrapper">
    <router-view></router-view>
  </div>
</template>

<script setup>
import TheNavigation from "./components/TheNavigation.vue";
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  margin-top: 100px;
}
</style>
