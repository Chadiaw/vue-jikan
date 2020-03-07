<template>
  <div id="app">
    <h1>Sample app using VueJS and jikanjs</h1>    
    <AnimeList></AnimeList>
  </div>
</template>

<script>
import AnimeList from "./components/AnimeList";

export default {
  name: "App",
  components: {
    AnimeList
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;  
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
	text-align: center;
}

</style>
