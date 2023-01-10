<template>
<nav class="main-nav">
    <router-link :to="{ name:'Home' }">Home</router-link>
    <router-link :to="{ name:'Movies' }">Movies</router-link>
    <router-link :to="{ name: 'TvShows' }">Tv Shows</router-link>
</nav>
</template>

<script>
</script>

<style>
nav.main-nav {
    font-size: 20px;
    display: flex;
    gap: 10px;
    justify-content: left;
    background-color: #032541;
    padding: 20px;
}

a.router-link-active.router-link-exact-active {
    color: #218c74;
}

nav.main-nav a {
    color: white;
    text-decoration: unset;
    font-size: 16px;
    font-weight: 600;
}
</style>
