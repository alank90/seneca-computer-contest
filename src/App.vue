<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <TheNavigation />
  <router-view></router-view>
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
