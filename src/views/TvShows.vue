<template>
<div class="popular-movie-header">Popüler Diziler</div>
<MovieCard :movies="tvShows"></MovieCard>
</template>

<script>
import MovieCard from '../components/MovieCard.vue';

export default {
    components: {
        MovieCard,
    },
    data() {
        return {
            tvShows: [],
        }
    },
    mounted() {
        fetch(
                'https://api.themoviedb.org/3/tv/popular?api_key=348088421ad3fb3a9d6e56bb6a9a8f80&language=en-US&page=1'
            )
            .then((response) => response.json())
            .then((data) => (this.tvShows = data.results))
            .catch((error) => console.log(error));
    },
}
</script>

<style scoped>
</style>
