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
          <img src="@/assets/images/card-1.jpg" alt="Auditorium" />
          <p>Thirds</p>
        </div>
        <div class="pure-u-1-3">
          <img src="@/assets/images/card-2.jpg" alt="Church" />
          <p>Thirds</p>
        </div>
        <div class="pure-u-1-3">
          <img src="@/assets/images/card-3.jpg" alt="Students" />
          <p>Thirds</p>
        </div>
      </div>
    </div>
  </div>
</template>

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

img[alt="Sienna logo"] {
  margin: 0 auto;
}

/* Double .main to add specificity cheaply. */
.main.main {
  background: #ffffff;
  position: relative;
  z-index: 3;
  margin-top: 30px;
  background-color: #f7f7f5b2;
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
</style>
