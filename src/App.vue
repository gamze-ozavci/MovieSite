<template>
<Navbar />
<div class="page-container">
    <router-view />
</div>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
    components: {
        Navbar,
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    margin: 0 auto;
    color: #f1f2f6;
}

body {
    background-color: white;
    margin: unset;
}

.page-container {
    max-width: 1400px;
    margin: 0 auto;
}
</style>
