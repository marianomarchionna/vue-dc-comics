<template>
    <footer>
        <div class="footer-top clearfix">
            <div class="container">
                <div class="top-left">
                    <div class="column">
                        <ul>
                            <span>DC COMICS</span>
                            <li v-for="(link, index) in dccomicslinks" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                        <ul>
                            <span>SHOP</span>
                            <li v-for="(link, index) in shoplinks" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                    </div>
                    <div class="column">
                        <ul>
                            <span>DC</span>
                            <li v-for="(link, index) in dclinks" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                    </div>
                    <div class="column">
                        <ul>
                            <span>SITES</span>
                            <li v-for="(link, index) in siteslinks" :key="index"><a href="">{{link.text}}</a></li>
                        </ul>
                    </div>
                </div>
                <div class="top-right">
                    <img src="@/assets/img/dc-logo-bg.png" alt="Logo DC">
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <div class="bottom-left">
                    <button>SIGN-UP NOW!</button>
                </div>
                <div class="bottom-right">
                    <span>FOLLOW US</span>
                    <div v-for="(link, index) in sociallinks" :key="index">
                        <a :href="link.url"><img :src="require(`../assets/${link.icon}`)" :alt="link.name"></a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import Links from '@/data/Links.js'

export default {
    name: 'Footer',
    data(){
        return{
            dccomicslinks: Links.dcComics,
            shoplinks: Links.Shop, 
            dclinks: Links.DC, 
            siteslinks: Links.Sites,
            sociallinks: Links.socials
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/general";
.footer-top {
    width: 100%;
    height: 350px;
    background-image: url('../assets/img/footer-bg.jpg');
    .container {
        width: 80%;
        height: 100%;
        .top-left {
            float: left;
            width: 40%;
            margin-top: 20px;
            display: flex;
            .column {
                width: calc(100% / 3);
                height: 100%;
                ul {
                    list-style: none;
                    span {
                        color: $white;
                        font-size: $big;
                        font-weight: $bold;
                        line-height: 3em;
                    }
                    li a {
                        text-decoration: none;
                        font-size: $semismall;
                        color: $white;
                        &:hover{
                            color: $primary-color;
                        }
                    }
                }
            }
        }
        .top-right {
            float: left;
            width: 60%;
            height: 100%;
            img{
                padding-left: 100px;
                object-fit: cover;
                width: 100%;
                height: 100%;
            }
        }
    }
}
.footer-bottom {
    height: 100px;
    width: 100%;
    background-color: $darkgray;
    .container {
        height: 100%;
        width: 80%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .bottom-left {
            button {
                border: 2px solid $primary-color;
                padding: 15px 25px;
                color: $white;
                font-size: $big;
                cursor: pointer;
                background-color: transparent;
                &:hover{
                    background-color: $primary-color;
                    color: $darkgray;
                    border: 2px solid $white;
                }
            }
        }
        .bottom-right {
            width: 35%;
            display: flex;
            justify-content: space-around;
            align-items: center;
            span {
                color: $primary-color;
                font-weight: $bold;
                font-size: $big;
            }
            div:hover img{
                height: 40px;
            }
        }
    }
}
</style>