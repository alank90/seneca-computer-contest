<template>
  <TheNavigation />
  <div class="wrapper">
    <router-view></router-view>
  </div>

  <TheFooter />
</template>

<script setup>
import TheNavigation from "./components/TheNavigation.vue";
import TheFooter from "@/components/TheFooter.vue";
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
