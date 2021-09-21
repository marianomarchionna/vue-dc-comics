<template>
  <div class="banner">
    <div class="container-banner">
      <div class="icon" v-for="(icon, index) in icons" :key="index">
        <img :src="require(`@/assets/${icon.url}`)" :alt="icon.text">
        <h3>{{icon.text.toUpperCase()}}</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'BlueBanner',
    data() {
        return {
            icons: [
                {   
                    url: 'img/buy-comics-digital-comics.png',
                    text: 'Digital Comics'
                },
                {   
                    url: 'img/buy-comics-merchandise.png',
                    text: 'DC Merchandise'
                },
                {   
                    url: 'img/buy-comics-subscriptions.png',
                    text: 'Subscriptions'
                },
                {   
                    url: 'img/buy-comics-shop-locator.png',
                    text: 'Shop Locator'
                },
                {   
                    url: 'img/buy-dc-power-visa.svg',
                    text: 'Power Visa'
                },
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/general";
.banner {
    background-color: $primary-color;
    height: 150px;
}
.container-banner {
  width: 70%;
  height: 100%;
  margin: 0 auto;
  @include center(vertical);
  justify-content: space-around;
}
.icon {
    height: 50px;
    @include center(vertical);
    cursor: pointer;    
    img{
      height: 100%; 
      max-width: 50px;
    }
    h3 {
      color: $white;
      font-size: $normal;
      padding: 0 10px;
    }
}

</style>