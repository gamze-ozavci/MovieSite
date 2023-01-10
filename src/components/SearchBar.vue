<template>
<div class="banner-container">
    <div class="title">
        <h2>Hoş Geldiniz.</h2>
        <h3>Milyonlarca film, TV şovu ve keşfedilecek kişi. Şimdi keşfedin.</h3>
    </div>
    <div class="search-bar-container">
        <form id="search-form" action="/search">
            <label>
                <input id="search-text" name="query" placeholder="Film, dizi, kişi ara..." value="">
            </label>
            <input id="search-button" type="submit" value="Search">
        </form>
    </div>
</div>
</template>

<script>
</script>

<style>
.banner-container {
    min-height: 300px;
    height: calc(100vh / 2.5);
    max-height: 360px;
    background-position: top center;
    background-size: cover;
    background-repeat: no-repeat;
    color: #fff;
    background-image: url("https://www.themoviedb.org/t/p/w1920_and_h600_multi_faces_filter(duotone,032541,01b4e4)/bcT8CaBIj086WVD7K529h78eujb.jpg");
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    padding: 60px 35px 0px;
    gap: 40px;
}

.title {
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    gap: 10px;
}

.banner-container h2 {
    font-size: 3em;
    margin: unset;
}

.banner-container h3 {
    font-size: 2em;
    margin: unset;
}

.search-bar-container {
    width: 100%;
}

#search-form {
    width: 100%;
    display: flex;
    align-items: center;
}

.banner-container label {
    width: 80%;
}

.banner-container .search {
    width: 100%;
}

#search-text {
    padding: 15px;
    width: 100%;
    border-radius: 25px;
    font-size: 15px;
    outline: 0 !important;
}

#search-button {
    padding: 0 35px;
    border: unset;
    height: 49px;
    border-radius: 40px;
    margin-left: -15px;
    font-size: 15px;
    cursor: pointer;
    background-image: linear-gradient(45deg, rgb(87 134 180 / 95%), hsl(119deg 40% 75%));
    color: white;
    font-weight: 600;
}
</style>
