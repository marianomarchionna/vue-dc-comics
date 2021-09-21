<template>
    <header>
        <div class="header-nav container">
            <div class="logo">
                <img src="@/assets/img/dc-logo.png" alt="logo.png">
            </div>
            <div class="nav-menu">
                <ul class="nav-items">
                    <li v-for="(link, index) in links" :key="index" class="nav-item" :class="(link.current) ? 'active' : null">
                        <a :href="link.url">{{link.text.toUpperCase()}}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
import Links from '@/data/Links.js'

export default {
    name: 'Header',
    data(){
        return{
            links: Links.headerLinks,
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/general";
.header-nav{
    height: 100px;
    @include center(vertical); 
    justify-content: space-between;
}

.logo {
    width: 70px;
    padding: 20px 0px;
    img{
        width: 100%;
    }
}

.nav-items{
    list-style: none; 
    display: flex; 
    font-size: 13px;
    font-weight: $bold; 
    line-height: 95px;
}

.nav-item{
  padding: 0px 14px;
  color: $darkgray;
  cursor: pointer;
  a{
    text-decoration: none;
    color: inherit;
    &:hover{
      color: $primary-color;
    }
  }
  &:hover{
    color: $primary-color;
    border-bottom: 5px solid $primary-color;
  }
  &.active{
      color: $primary-color;
      border-bottom: 5px solid $primary-color;
  }
}
</style>