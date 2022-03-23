<template>
  <div class="home">
    <h1>Scarsdale Computer Club</h1>
    <img
      class="pure-img"
      alt="Sienna logo"
      src="@/assets/images/siena-logo-cs-white.png"
    />
    <h2>High School Programming Contest</h2>
    <div class="main main-raised">
      <div id="info" class="section">
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
          <div class="card-header">
            <img
              class="pure-img-responsive"
              src="@/assets/images/card-1.jpg"
              alt="Auditorium"
            />
          </div>
          <div class="card-body">
            <h6 class="card-category text-info">
              <i class="material-icons">calendar_today</i>When?
            </h6>
            <h4 class="card-title">Friday, April 8th 2022</h4>
            <p class="card-description">Last Afternoon / Early Evening</p>
            <p>
              Email <b>matthews@siena.edu</b> if you are interested in
              participating
            </p>
            <p><button class="pure-button btn btn-info">Details</button></p>
          </div>
        </div>

        <div class="pure-u-1-3">
          <img
            class="pure-img-responsive"
            src="@/assets/images/card-2.jpg"
            alt="Church"
          />
          <p class="card-description">Thirds</p>
        </div>
        <div class="pure-u-1-3">
          <img
            class="pure-img-responsive"
            src="@/assets/images/card-3.jpg"
            alt="Students"
          />
          <p>Thirds</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import "@/assets/css/card.css";

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

/* Double .main to add specificity cheaply. */
.main.main {
  background: #ffffff;
  position: relative;
  z-index: 3;
  margin-top: 30px;
  background-color: #e6e9e6b6;
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
