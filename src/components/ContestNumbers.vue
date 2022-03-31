<template>
  <div class="grid">
    <!-- eslint-disable-next-line vue/no-v-for-template-key -->
    <template v-for="n in 3" :key="n">
      <h5 class="mainTitle1">{{ mainTitle[n - 1] }}</h5>
      <h6 class="'sub-title' + n">{{ subTitle[n - 1] }}</h6>

      <div class="`card${1 + ((n - 1) * 4)}`">
        <ContestCard
          :prop-card-info="cardInfo1"
          :propCardTitle="cardTitle[1 + (n - 1) * 4]"
        />
      </div>
      <div class="`card${2 + ((n - 1) * 4)}`">
        <ContestCard
          :prop-card-info="cardInfo2"
          :propCardTitle="cardTitle[2 + (n - 1) * 4]"
        />
      </div>
      <div class="`card${3 + ((n - 1) * 4)}`">
        <ContestCard
          :prop-card-info="cardInfo3"
          :propCardTitle="cardTitle[3 + (n - 1) * 4]"
        />
      </div>
      <div class="`card${4 + ((n - 1) * 4)}`">
        <ContestCard
          :prop-card-info="cardInfo4"
          :propCardTitle="cardTitle[4 + (n - 1) * 4]"
        />
      </div>
    </template>
  </div>
</template>

<script setup>
import ContestCard from "@/components/ContestCard.vue";

const cardInfo1 = {
  subtitle: "DIVISIONS",
  materialIcon: "view_stream",
  bgColor: "#069eaf",
};

const cardInfo2 = {
  subtitle: "SCHOOLS",
  materialIcon: "school",
  bgColor: "#3f9543",
};

const cardInfo3 = {
  subtitle: "TEAMS",
  materialIcon: "people",
  bgColor: "#ca2061",
};

const cardInfo4 = {
  subtitle: "STUDENTS",
  materialIcon: "emoji_people",
  bgColor: "#9c3ab4",
};

const mainTitle = ["2021 Numbers", "2020 Numbers", "2019 Numbers"];
const subTitle = [
  "Virtual Only",
  "Before the contest was cancelled due to COVID, the following had signed up...",
  "",
];
const cardTitle = [2, 19, 60, 236, 2, 21, 80, 315, 2, 18, 59, 234];
</script>

<style scoped>
.grid {
  display: grid;
  grid-gap: 1rem;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: fit-content;
  max-width: 1200px;
  grid-template-areas:
    "..... main1  main1 ......"
    "..... sub1  sub1 ......"
    "card1 card2 card3 card4"
    "..... main2  main2 ......"
    "..... sub2  sub2 ......"
    "card5 card6 card7 card8";
}

.main-title1 {
  grid-area: main1;
  margin: 100px 0 -20px 0;
}

.main-title2 {
  grid-area: main2;
  margin: 100px 0 -20px 0;
}

.sub-title1 {
  grid-area: sub1;
  font-size: 1.1rem;
}

.sub-title2 {
  grid-area: sub2;
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
.card5 {
  grid-area: card5;
}

.card6 {
  grid-area: card6;
}

.card7 {
  grid-area: card7;
}

.card8 {
  grid-area: card8;
}
</style>
