<template>
  <div class="grid">
    <h5 class="main-title">2021 Numbers</h5>
    <h6 class="sub-title">Virtual Only</h6>
    <div class="card1">
      <ContestCard />
    </div>
    <div class="card2"></div>
    <div class="card3"></div>
    <div class="card4"></div>
  </div>
</template>

<script setup>
import ContestCard from "@/components/ContestCard.vue";
</script>

<style scoped>
.grid {
  display: grid;
  grid-gap: 1rem;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: fit-content;
  max-width: 1200px;
  grid-template-areas:
    "..... main  main ......"
    "..... sub1  sub1 ......"
    "card1 card2 card3 card4";
}

.main-title {
  grid-area: main;
  margin: 100px 0 -20px 0;

}

.sub-title {
  grid-area: sub1;
  font-size: 1.1rem;
}
.card1 {
  grid-area: card1;
}
.card2 {
  grid-area: card2;
}
.card3 {
  grid-area: card3;
}

.card4 {
  grid-area: card4;
}
</style>
