<template>
    <div class="popular-movie-header">Popüler Filmler</div>
    <MovieCard :movies="movies"></MovieCard>
</template>

<script>
import MovieCard from '../components/MovieCard.vue';

export default {
    components: {
        MovieCard,
    },
    data() {
        return {
            movies: [],
        }
    },
    mounted() {
        fetch(
                'https://api.themoviedb.org/3/movie/now_playing?api_key=348088421ad3fb3a9d6e56bb6a9a8f80&language=en-US&page=1'
            )
            .then((response) => response.json())
            .then((data) => (this.movies = data.results))
            .catch((error) => console.log(error));
    },
}
</script>

<style scoped>
</style>
