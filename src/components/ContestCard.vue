<template>
  <div
    class="card-container"
    :style="{ backgroundColor: props.propCardInfo.bgColor }"
  >
    <h3 class="card-title">{{ props.propCardInfo.title }}</h3>
    <h4 class="sub-title">{{ props.propCardInfo.subtitle }}</h4>
    <div class="icon">
      <i class="material-icons">{{ props.propCardInfo.materialIcon }}</i>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  propCardInfo: {
    type: Object,
  },
});
</script>

<style scoped>
.card-container {
  width: 100%;
  height: 300px;
  border-radius: 6px;
}

.card-title {
  color: #fff;
  padding-top: 40px;
  font-size: 3rem;
  font-weight: 700;
}

.sub-title {
  color: #fff;
  padding-top: 30px;
  font-size: 1.1rem;
  font-weight: 700;
}

.icon {
  font-size: 55px;
  border: 1px solid #e5e5e5;
  border-color: rgba(255, 255, 255, 0.25);
  width: 130px;
  height: 130px;
  margin: 20px auto;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.material-icons {
  font-family: "Material Icons";
  font-weight: normal;
  font-style: normal;
  font-size: 40px;
  max-width: 50px;
  line-height: 1;
  letter-spacing: normal;
  text-transform: none;
  white-space: nowrap;
  word-wrap: normal;
  direction: ltr;
}
</style>
