<template>
  <div class="container">
    <a href=""><span class="material-icons">keyboard_arrow_up</span></a>
  </div>
</template>

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
