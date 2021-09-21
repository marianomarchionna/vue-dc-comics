<template>
    <div class="jumbotron">
        <img src="@/assets/img/jumbotron.jpg" alt="">
    </div>
</template>

<script>
export default {
    name: 'Jumbotron'
}
</script>

<style scoped lang="scss">
.jumbotron{
    height: 350px;
    img{
        height: 100%;
        width: 100%;
        object-position: top;
        object-fit: cover;
    };
}
</style>