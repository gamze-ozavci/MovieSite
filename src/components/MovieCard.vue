<template>
<div class="movie-card-container" v-if="movies.length">
    <div class="movie-card"
        v-for="movie in movies"
        :key="movie.id">
        <img class="movies-image"
            :src="`https://image.tmdb.org/t/p/w220_and_h330_face${ movie.poster_path }`">
        <div class="movies-title">
            {{ movie.title || movie.name }}
        </div>
        <div class="reviews">
        </div>
        <div class="movie-date">{{ movie.release_date || movie.first_air_date }}</div>
    </div>
</div>
<div v-else>
    <p>Diziler yükleniyor</p>
</div>
</template>

<script>
export default {
    props: {
        movies: []
    },
}
</script>

<style>
.movie-card-container {
    display: flex;
    gap: 10px;
    width: 90%;
    flex-wrap: wrap;
    margin: auto;
}

.movie-card {
    width: 150px;
    margin: 20px auto;
    padding: 5px;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    color: #212121;
    gap: 8px;
    align-items: center;
    border-radius: 20px;
}

.movie-card:hover {
    box-shadow: 1px 0px 8px rgb(2 2 2 / 30%);
}

.movies-image {
    border-radius: 20px;
    width: 135px;
}

.movies-title {
    font-weight: 800;
    height: 50px;
}

.movie-date {
    color: #a1a1a1;
    font-weight: 700;
}
</style>
