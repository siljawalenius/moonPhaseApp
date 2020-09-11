

<template>
  <div class="moon-holder">
    <slot class="searchBar"> </slot>

    <span class="curLocation"> The Middle of Nowhere </span>
    <img class="moon-img" src="luna/src/assets/default.png" />
    <h1>Phase of moon</h1>
  </div>
</template>

<script>

import { differenceInDays } from 'date-fns'

export default {
  name: "MoonPhase",

  methods: {
    getMoonPhase() {
      const fullMoon = new Date(2020, 8, 3, 0, 0, 0);
      const cycle = 29.53;

      const now = new Date();

      // using the date-fns library
      const diff = differenceInDays(now, fullMoon);
      const diffCycle = diff % cycle;

      const text = document.querySelector("div.today");


        //TODO: REMEMBER TO PASS THROUGH MORE PHASES
      if (diffCycle < 3) {
        text.innerHTML = "Full Moon";
      } else if (diffCycle < 8) {
        text.innerHTML = "Waning";
      } else {
        text.innerHTML = "New moon";
      }
    },
  },
};
</script>

<style scoped>
.moon-holder {
  background-color: midnightblue;
  color: #fff;
}
</style>
