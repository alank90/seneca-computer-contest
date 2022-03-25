<template>
  <header>
    <div class="card-header">
      <slot name="header">
        <img
          class="pure-img-responsive"
          :src="props.propCardInfo.img"
          alt="Auditorium"
        />
      </slot>
    </div>
  </header>

  <main>
    <div class="card-body">
      <div class="card-body">
        <h6 class="card-category text-info">
          <i class="material-icons">{{ props.propCardInfo.materialIcon }}</i
          >{{ props.propCardInfo.category }}
        </h6>
        <h4 class="card-title">{{ props.propCardInfo.title }}</h4>

        <slot name="description">Default Material</slot>

        <slot name="button">
          <button class="pure-button btn btn-info">Details</button>
        </slot>
      </div>
    </div>
  </main>
</template>

<script setup>
import { defineProps } from "vue";
import "@/assets/css/card.css";

const props = defineProps({
  propCardInfo: {
    type: Object,
  },
});
</script>
