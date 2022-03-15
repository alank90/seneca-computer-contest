<template>
  <TheNavigation />
  <GoBack />

  <router-view></router-view>
</template>

<script setup>
import TheNavigation from "./components/TheNavigation.vue";
import GoBack from "@/components/GoBack.vue";
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

* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

/*
 * -- BASE STYLES --
 * Most of these are inherited from Base, but I want to change a few.
 */
body {
  line-height: 1.7em;
  color: #7f8c8d;
  font-size: 13px;
  background-image: url("@/assets/images/keyboard_programming.jpg");
  background-repeat: no-repeat;
  background-size: ;
}

h1,
h2,
h3,
h4,
h5,
h6,
label {
  color: #a2ded0;
}

.pure-img-responsive {
  max-width: 100%;
  height: auto;
}

/*
 * -- LAYOUT STYLES --
 * These are some useful classes which I will need
 */
.l-box {
  padding: 1em;
}

.l-box-lrg {
  padding: 2em;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.is-center {
  text-align: center;
}
</style>
