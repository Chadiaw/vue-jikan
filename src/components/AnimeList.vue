<template>
  <div class="anime">    
    <ul v-if="animes.length">
			<AnimeItem
				v-for="anime in animes"
				:key="anime.mal_id"
				:anime="anime"
			/>
	</ul>
  </div>
</template>

<script>  
import AnimeItem from './AnimeItem.vue'
import jikan from 'jikanjs';

export default {
  name: 'AnimeList',
  data() {
    return {
      animes: {
        type: Array
      }
    }
  },
  components: {
    AnimeItem
  },
  created() {
    jikan.loadTop('anime').then((response) => {        
        this.animes = response.top;
    }).catch((err) => {
        console.error(err);
    });

  }
}
</script>
<style lang="scss">
  .anime {
    height: 80vh;
    width: 100%;
  }
</style>