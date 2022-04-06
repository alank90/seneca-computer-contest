<template>
  <div class="card-container card">
    <h3 class="card-title">{{ props.propCardTitle }}</h3>
    <h4 class="sub-title">{{ props.propCardInfo.subtitle }}</h4>
    <div class="icon">
      <i class="material-icons">{{ props.propCardInfo.materialIcon }}</i>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
import "@/assets/css/card.css";

const props = defineProps({
  propCardInfo: {
    type: Object,
  },
  propCardTitle: {
    type: Number,
  },
});
</script>

<style scoped>
.card-container {
  background-color: v-bind("props.propCardInfo.bgColor");
}
</style>
