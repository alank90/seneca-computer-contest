<template>
  <div class="container" v-show="isVisible" @click="backToTop">
    <a href=""><span class="material-icons">keyboard_arrow_up</span></a>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
let isVisible = ref(false);

const scrollListener = () => {
  if (window.scrollY > 2700) {
    isVisible.value = true;
  } else {
    isVisible.value = false;
  }
};

const backToTop = () => {
  window.scrollTo({
    top: 0,
    left: 0,
    behavior: "smooth",
  });
};

onMounted(() => {
  window.addEventListener("scroll", scrollListener);
});

onUnmounted(() => {
  window.removeEventListener("scroll", backToTop);
});
</script>

<style scoped>
.container {
  position: absolute;
  left: 50%;
  width: 100px;
  height: 100px;
  border: 3px solid var(--sienna-yellow);
  border-radius: 50%;
  transform: translateY(-50px);
  z-index: 999;
}

a {
  font-size: 0.9rem;
  text-align: center;
}

span {
  transform: scale(1.7);
  margin-top: 10px;
}
</style>
