<template>
  <!--HTML -->

  <div id="app">
    <main> 
      <SearchBar></SearchBar>
      <MoonPhase></MoonPhase>
      </main>
    
  </div>
</template>

<!-- JS -->
<script>
//import HelloWorld from "./components/HelloWorld.vue";
import MoonPhase from "./components/MoonPhase.vue"
import SearchBar from "./components/SearchBar.vue"

export default {
  name: "App",
  props: [],
  data() {
    return {
      url: "https://api.worldweatheronline.com/premium/v1/astronomy.ashx",
      city: "",
      key: 'ae253e88fa834f4486e10006201109',
      includelocation: true
    };
  },
  components: {
    //HelloWorld,
    MoonPhase,
    SearchBar
  },
};
</script>

<!-- CSS -->
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

main{
  height:100vh;

}

</style>
