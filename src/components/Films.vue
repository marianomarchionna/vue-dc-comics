<template>
    <div class="film-section">
        <div class="current-series">
            <h3>CURRENT SERIES</h3>
        </div>
        <div class="film-container">
            <FilmCard 
            v-for="(film, index) in films" 
            :key="index"
            :film="film"
            />
        </div>
        <button>LOAD MORE</button>
    </div>
</template>

<script>
import FilmCard from '@/components/FilmCard.vue'
import Links from '@/data/Links.js'

export default {
    name: 'Films',
    components: {
        FilmCard
    },
    data(){
        return{
            films: Links.filmLinks,
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/general.scss';
.film-section {
    width: 100%;
    background-color: $back-films;
    .current-series {
        color: $white;
        font-size: 18px;
        font-weight: $bold;
        background-color: $primary-color;
        display: inline-block;
        padding: 10px 20px;
        position: relative;
        top: -20px;
        left: 15%;
        h3 {
            font-size: $big;
        }
    }
    .film-container {
        display: flex;
        flex-wrap: wrap;
        width: 70%;
        margin: 0 auto;
    }
    button {
        background-color: $primary-color; 
        border: none;
        color: white;
        padding: 10px 40px;
        font-size: $small;
        cursor: pointer;
        margin: 20px 0;
        position: relative;
        left: 50%;
        transform: translate(-50%);
    }
}
</style>