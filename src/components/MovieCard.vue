<template>
  <div class="movie-card">
    <div class="movie-image">
      <img :src="movie.image" :alt="movie.title">
      <button class="close-btn" @click="$emit('remove', movie.id)">×</button>
    </div>
    <div class="movie-info">
      <h3>{{ movie.title }}</h3>
      <p>{{ movie.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MovieCard',
  props: {
    movie: {
      type: Object,
      required: true
    }
  },
  emits: ['remove']
}
</script>

<style scoped>
@import '../assets/css/movie-card.css';
</style>
