<template>
  <div class="film-card">
    <img :src="film.thumb" :alt="film.series">
    <p>{{ film.series.toUpperCase() }}</p>
  </div>
</template>

<script>
export default {
  name: 'FilmCard',
  props: ['film']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/style/general.scss';
.film-card {
    cursor: pointer;
    flex-basis: 14%;
    margin: 10px;
    img {
        height: 135px;
        width: 135px;
        object-position: top;
        object-fit: cover;
    }
    p {
        padding: 10px 0;
        font-size: $small;
        color: $white;
    }
}
</style>