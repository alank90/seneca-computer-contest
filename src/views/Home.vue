<template>
  <div class="home">
    <h1>Scarsdale Computer Club</h1>

    <div class="main main-raised">
      <div id="info" class="section">
        <img
          class="pure-img"
          alt="Sienna logo"
          src="@/assets/images/siena-logo-cs-white.png"
        />
        <h2><span>Sienna College</span>High School Programming Contest</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam
          quaerat ullam repudiandae eaque, cum repellat assumenda mollitia
          inventore fugit soluta officiis suscipit ratione quidem, saepe
          voluptas aspernatur impedit? Aperiam similique inventore esse error
          pariatur, corrupti placeat distinctio magni ad. Veritatis.
        </p>
      </div>

      <div class="pure-g">
        <div class="pure-u-1-3">
          <FrontPageCard :propCardInfo="cardInfo1">
            <template #header> </template>

            <template #description>
              <p class="card-description" v-html="cardInfo1.description"></p>
            </template>

            <template #button></template>
          </FrontPageCard>
        </div>

        <div class="pure-u-1-3">
          <FrontPageCard :propCardInfo="cardInfo2">
            <template #header> </template>

            <template #description>
              <p class="card-description" v-html="cardInfo2.description"></p>
            </template>

            <template #button>
              <button class="pure-button btn btn-success">
                {{ cardInfo2.button1 }}
              </button>
              <button
                :style="{ marginLeft: cardInfo2.button2.marginLeft }"
                class="pure-button btn btn-success"
              >
                {{ cardInfo2.button2.label }}
              </button>
            </template>
          </FrontPageCard>
        </div>

        <div class="pure-u-1-3">
          <FrontPageCard :propCardInfo="cardInfo3">
            <template #header></template>

            <template #description>
              <p class="card-description" v-html="cardInfo3.description"></p>
            </template>

            <template #button>
              <button class="pure-button btn btn-primary">PHOTOS</button>
            </template>
          </FrontPageCard>
        </div>
      </div>

      <ContestDetails></ContestDetails>

      <ContestNumbers></ContestNumbers>
    </div>
  </div>
</template>

<script setup>
import FrontPageCard from "@/components/FrontPageCard.vue";
import ContestDetails from "@/components/ContestDetails.vue";
import ContestNumbers from "@/components/ContestNumbers.vue";

// ======= Vars =================== //
const cardInfo1 = {
  materialIcon: "calendar_today",
  img: "src/assets/images/card-1.jpg",
  alt: "Auditorium",
  title: "Friday, April 8th 2022",
  category: "WHEN?",
  description:
    "<p class='card-description'>Last Afternoon / Early Evening</p><p class='card-description'> Email <b>matthews@siena.edu</b> if you are interested in participating</p>",
};

const cardInfo2 = {
  materialIcon: "location_on",
  img: "src/assets/images/card-2.jpg",
  alt: "School Picture",
  title: "Siena College, Loudonville NY",
  category: "WHERE?",
  description:
    "<p class='card-description'>Siena's Computer Science Department has hosted the contest on campus since 1986.</p>",
  button1: "SIENNA EDU",
  button2: { label: "CS DEPT", marginLeft: 5 + "px" },
};

const cardInfo3 = {
  materialIcon: "helper",
  img: "src/assets/images/card-3.jpg",
  alt: "Students",
  title: "Fun & Excitement",
  category: "WHY?",
  description:
    "<p class='card-description'>Programming contests are competitive and fun with pizza, cookies and drinks provided.</p>",
};
</script>

<style scoped>
h1,
h2 {
  color: var(--sienna-yellow);
  font-family: var(--noto);
}

h2 {
  margin-top: 15px;
}

h2 > span {
  display: block;
  color: var(--sienna-green);
}

h4 ~ p {
  font-size: 14px;
  margin: 0 0 10px;
}

img[alt="Sienna logo"] {
  margin: 0 auto;
}

.main .pure-g {
  margin-bottom: 100px;
}

/* Double .main to add specificity cheaply. */
.main.main {
  background: #ffffff;
  position: relative;
  z-index: 3;
  margin-top: 30px;
  background-color: #1E3803da;
  padding: 0 50px;
}

.main-raised {
  margin: -60px 30px 0px;
  border-radius: 6px;
  box-shadow: 0 16px 24px 2px rgba(0, 0, 0, 0.14),
    0 6px 30px 5px rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(0, 0, 0, 0.2);
}

.section,
.section-image {
  background-position: center center;
  background-size: cover;
  padding: 70px 0;
}

/* Add a gutter to Pure's Columns */
.pure-g {
  margin: 0 -1em;
}

.pure-g > div {
  padding: 0 1em;
}
</style>
