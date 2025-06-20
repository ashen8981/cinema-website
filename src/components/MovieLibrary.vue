<template>
  <section id="library" class="movie-library">
    <div class="container">
      <div class="library-header">
        <h2>Collect your favourites</h2>
        <SearchBar v-model="searchQuery" />
      </div>
      
      <div class="movies-grid">
        <MovieCard 
          v-for="movie in filteredMovies" 
          :key="movie.id"
          :movie="movie"
          @remove="removeMovie"
        />
      </div>
    </div>
  </section>
</template>

<script>
import SearchBar from './SearchBar.vue'
import MovieCard from './MovieCard.vue'
import batmanImg from '@/assets/images/Batman.jpg'
import wildWestImg from '@/assets/images/WildWest.jpg'
import spidermanImg from '@/assets/images/Spiderman.jpg'

export default {
  name: 'MovieLibrary',
  components: {
    SearchBar,
    MovieCard
  },
  data() {
    return {
      searchQuery: '',
      movies: [
        {
          id: 1,
          title: 'Batman Returns',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy eirmod tempor invidunt ut...',
          image: batmanImg
        },
        {
          id: 2,
          title: 'Wild Wild West',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy eirmod tempor invidunt ut...',
          image: wildWestImg
        },
        {
          id: 3,
          title: 'The Amazing Spiderman',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy eirmod tempor invidunt ut...',
          image: spidermanImg
        }
      ]
    }
  },
  computed: {
    filteredMovies() {
      if (!this.searchQuery) return this.movies
      return this.movies.filter(movie => 
        movie.title.toLowerCase().includes(this.searchQuery.toLowerCase())
      )
    }
  },
  methods: {
    removeMovie(movieId) {
      this.movies = this.movies.filter(movie => movie.id !== movieId)
    }
  }
}
</script>

<style scoped>
@import '../assets/css/movie-library.css';
</style>
