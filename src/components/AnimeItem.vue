<template>
  <p>
    {{ anime.rank }} - {{ anime.title }} --- Score: {{ anime.score }} -- ID: {{ anime.mal_id }}    
  </p>
</template>

<script>
export default {
  props: {
    anime: {
      type: Object,
      required: true
    }
  }
}
</script>