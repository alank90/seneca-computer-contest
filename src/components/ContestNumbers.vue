<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div class="grid">
    <template v-for="n in 3">
      <h5 :class="numberSectionInfo[n - 1].titleClass">
        {{ numberSectionInfo[n - 1].title }}
      </h5>
      <h6 :class="numberSectionInfo[n - 1].subtitleClass">
        {{ numberSectionInfo[n - 1].subtitle }}
      </h6>

      <div :class="numberSectionInfo[n - 1].cardInfo1.gridArea">
        <ContestCard
          :prop-card-info="numberSectionInfo[n - 1].cardInfo1"
          :propCardTitle="
            cardTitle[1 + (numberSectionInfo[n - 1].id - 1) * 4 - 1]
          "
        />
      </div>
      <div :class="numberSectionInfo[n - 1].cardInfo2.gridArea">
        <ContestCard
          :prop-card-info="numberSectionInfo[n - 1].cardInfo2"
          :propCardTitle="
            cardTitle[2 + (numberSectionInfo[n - 1].id - 1) * 4 - 1]
          "
        />
      </div>
      <div :class="numberSectionInfo[n - 1].cardInfo3.gridArea">
        <ContestCard
          :prop-card-info="numberSectionInfo[n - 1].cardInfo3"
          :propCardTitle="
            cardTitle[3 + (numberSectionInfo[n - 1].id - 1) * 4 - 1]
          "
        />
      </div>
      <div :class="numberSectionInfo[n - 1].cardInfo4.gridArea">
        <ContestCard
          :prop-card-info="numberSectionInfo[n - 1].cardInfo4"
          :propCardTitle="
            cardTitle[4 + (numberSectionInfo[n - 1].id - 1) * 4 - 1]
          "
        />
      </div>
    </template>
  </div>
</template>

<script setup>
import ContestCard from "@/components/ContestCard.vue";

// Template info array for the cards section
const numberSectionInfo = [
  {
    id: 1,
    title: "2021 NUMBERS",
    titleClass: "main-title1",
    subtitle: "VIRTUAL ONLY",
    subtitleClass: "sub-title1",
    cardInfo1: {
      subtitle: "DIVISIONS",
      materialIcon: "view_stream",
      bgColor: "#069eaf",
      gridArea: "card1",
    },
    cardInfo2: {
      subtitle: "SCHOOLS",
      materialIcon: "school",
      bgColor: "#3f9543",
      gridArea: "card2",
    },
    cardInfo3: {
      subtitle: "TEAMS",
      materialIcon: "people",
      bgColor: "#ca2061",
      gridArea: "card3",
    },
    cardInfo4: {
      subtitle: "STUDENTS",
      materialIcon: "emoji_people",
      bgColor: "#9c3ab4",
      gridArea: "card4",
    },
  }, // End of 1st array element
  {
    id: 2,
    title: "2020 NUMBERS",
    titleClass: "main-title2",
    subtitle:
      "Before the contest was cancelled due to COVID, the following had signed up...",
    subtitleClass: "sub-title2",
    cardInfo1: {
      subtitle: "DIVISIONS",
      materialIcon: "view_stream",
      bgColor: "#069eaf",
      gridArea: "card5",
    },
    cardInfo2: {
      subtitle: "SCHOOLS",
      materialIcon: "school",
      bgColor: "#3f9543",
      gridArea: "card6",
    },
    cardInfo3: {
      subtitle: "TEAMS",
      materialIcon: "people",
      bgColor: "#ca2061",
      gridArea: "card7",
    },
    cardInfo4: {
      subtitle: "STUDENTS",
      materialIcon: "emoji_people",
      bgColor: "#9c3ab4",
      gridArea: "card8",
    },
  },
  {
    id: 3,
    title: "2019 NUMBERS",
    titleClass: "main-title3",
    subTitle: "",
    subtitleClass: "sub-title3",
    cardInfo1: {
      subtitle: "DIVISIONS",
      materialIcon: "view_stream",
      bgColor: "#069eaf",
      gridArea: "card9",
    },
    cardInfo2: {
      subtitle: "SCHOOLS",
      materialIcon: "school",
      bgColor: "#3f9543",
      gridArea: "card10",
    },
    cardInfo3: {
      subtitle: "TEAMS",
      materialIcon: "people",
      bgColor: "#ca2061",
      gridArea: "card11",
    },
    cardInfo4: {
      subtitle: "STUDENTS",
      materialIcon: "emoji_people",
      bgColor: "#9c3ab4",
      gridArea: "card12",
    },
  }, // End Object
];

const cardTitle = [2, 19, 60, 236, 2, 21, 80, 315, 2, 18, 59, 234];
</script>

<style scoped>
.grid {
  display: grid;
  grid-gap: 1rem;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: auto;
  max-width: 1200px;
  margin: 0 auto;
  grid-template-areas:
    ". main1  main1 ."
    ". sub1  sub1 ."
    "card1 card2 card3 card4"
    ". main2  main2 ."
    ". sub2  sub2 ."
    "card5 card6 card7 card8"
    ". main3  main3 ."
    ". sub3  sub3 ."
    "card9 card10 card11 card12";
}

.main-title1 {
  grid-area: main1;
  margin: 100px 0 -20px 0;
}

.main-title2 {
  grid-area: main2;
  margin: 100px 0 -20px 0;
}
.main-title3 {
  grid-area: main3;
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
.sub-title3 {
  grid-area: sub3;
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
.card9 {
  grid-area: card9;
}
.card10 {
  grid-area: card10;
}
.card11 {
  grid-area: card11;
}
.card12 {
  grid-area: card12;
}
</style>
