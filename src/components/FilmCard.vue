<script setup>

defineProps({
    filmTitle: String,
    imageSrc: String,
    filmDirector: String
})

</script>

<template>
    <div class="film-card">
        <h2 class="film-title">{{filmTitle}}</h2>
        <p class="director-wrapper"><span class="director">Director </span>: <em>{{filmDirector}}</em></p>
        <img :src="imageSrc"/>
    </div>
</template>

<style>
.film-title {
    box-sizing: border-box;
    margin: 0px;
    padding: 5px;
}

.director {
    font-weight: 300;
    font-size: larger;
}
.director-wrapper {
    margin: 0;
    padding-bottom: 6px;
}

.film-card {
    border-radius: 20px;
    overflow: hidden;
    cursor: pointer;
    text-align: center;
    margin: 0px 20px 16px 20px;
    background-color: #000;
    color: #fff;
    box-shadow: -5px 5px 0px 0px #D3D3D3;
    width: 400px;
}
.film-card :hover {
    opacity: 0.5;
    transition: 300ms;
}

img {
    display: block;
    width: 100%;
    height: 300px;
}
</style>
