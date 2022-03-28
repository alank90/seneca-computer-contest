<template>
  <div class="container">
    <div class="col-1">
      <h4 class="item-a">2022 Contest Details</h4>
      <ul>
        Tentative Schedule
        <li>3:00pm to 4:00pm Arrive and check-in</li>
        <li>4:00pm to 4:30pm. Green teams orientation</li>
        <li>4:30pm to 5:15pm. Green teams compile and submission testing</li>
        <li>4:30pm to 5:00pm Gold teams orientation</li>
        <li>5:00pm to 5:15pm. Gold teams compile and submission testing</li>
        <li>
          4:30pm to 5:30pm. Remote teams join zoom contest session (Remote teams
          orientation will be held remotely before April 8)
        </li>
        <li>5:30pm to 8:30pm. Contest (and pizza ...)</li>
        <li>8:30pm to 8:40pm. Clean up work spaces, make copies of work</li>
        <li>8:45pm to 9:00pm. Trophy Presentation</li>
      </ul>
    </div>

    <div class="col-2">
      <h4>Our contest features two levels</h4>

      <div class="green">
        <h5>Green</h5>
        <p>
          Green level problems will be geared to students enrolled in their
          first programming course and similar in difficulty to problems 1 to 5
          in past contests
        </p>
      </div>

      <div class="gold">
        <h5>Gold</h5>
        <p>
          Gold level problems are geared towards students with two years of
          programming experience and similar in difficulty to problems 4 to 7 in
          past contests.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 30px 1fr 1fr;
  grid-template-rows: 1fr;
  gap: 0px 100px;
  grid-auto-flow: row;
  grid-template-areas: ". . .";
}

.col-1 {
  grid-column: 2 / span 1;
}

.col-2 {
  grid-column: 3 / span 1;
}

ul {
  font-size: 1.2rem;
}

li {
  font-size: 0.9rem;
  text-align: start;
}

.green {
  width: 400px;
  height: auto;
  background-color: #479d4b;
  border-radius: 4px;
  color: rgba(255, 255, 255, 0.8);
  padding: 0 5px 5px;
}
.green h5 {
  font-size: 1rem;
  margin-top: 20px;
}
.green p {
  font-size: 0.9rem;
  text-align: start;
  padding-left: 5px;
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.2em;
}

.gold {
  width: 400px;
  height: auto;
  background-color: #fa9214;
  border-radius: 4px;
  color: rgba(255, 255, 255, 0.8);
  padding: 0 5px 5px;
}
.gold h5 {
  font-size: 1rem;
  margin-top: 20px;
}
.gold p {
  font-size: 0.9rem;
  text-align: start;
  padding-left: 5px;
  line-height: 1.2em;
}
</style>
