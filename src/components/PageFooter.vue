<script>
    import { store } from '../store.js'

    export default{
        name: 'PageFooter',
        props:{
            footerInfo: Object,
        },
        data(){
            return{
                store,
            }
        },
        methods: {
            getImageUrl(name) {
                return new URL(`${name}`, import.meta.url).href;
            }
        },
    }
</script>

<template>
    <footer>
        <!-- Footer link/contacs/socials -->
        <div class="container">
            <div class="row">
                <div class="col-33">
                    <img class="footer-logo" :src="getImageUrl(footerInfo.leftCol[0].logo)" alt="logo">
                    <p>{{ footerInfo.leftCol[0].paragraph }}</p>
                    <div class="social-wrapper">
                        <a  v-for="social in footerInfo.leftCol[0].socialLinks" href="#">
                            <i :class="social.social"></i>
                        </a>
                    </div>
                </div>
                <div class="col-33">
                    <h3>{{ footerInfo.midCol[0].title}}</h3>
                    <ul>
                        <li v-for="post in footerInfo.midCol[0].posts">
                            <a class="d-flex jst-cntr" href="#">
                                <i class="fa-solid fa-chevron-right"></i>
                                <div class="post">{{ post.link }}</div>
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-33">
                    <h3>{{ footerInfo.rightCol[0].title }}</h3>
                    <div class="address">{{ footerInfo.rightCol[0].contacts[0].address }}</div>
                    <div class="mobile">{{ footerInfo.rightCol[0].contacts[0].mobile }}</div>
                    <div>{{ footerInfo.rightCol[0].contacts[0].email }}</div>
                </div>
            </div>
        </div>
        <!-- /Footer link/contacs/socials -->

        <!-- Footer copyright -->
        <div class="footer-container">
            <div class="copyright d-flex jst-cntr algn-cntr">
                <i class="fa-regular fa-copyright"></i>
                <div>Copyright 2012 - 2020 | Avada theme by</div>
                <a href="#">Theme Fusion</a>
                <div> | All rights reserved | Powered by </div>
                <a href="#">WordPress</a>
            </div>
        </div>
        <!-- /Footer copyright -->
    </footer>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

footer{
    background-color: $palette-black;
    color: $palette-white;
    .container{
        .row{
            padding: 80px 0;
            .col-33{
                font-size: 20px;
                margin-bottom: 40px;
                width: calc(100% / 3);
                text-align: center;
                img, h3{
                    height: 52px;
                }
                h3{
                    display: flex;
                    justify-content: center;
                    align-items: end;
                }
                p{
                    margin: 40px 0;
                    line-height: 1.5;
                }
                .footer-logo{
                    max-width: 300px;
                }
                .social-wrapper{
                    i{
                        color: $palette-red;
                        margin-right: 20px;
                        font-size: 20px;
                    }
                }
                li{
                    list-style: none;
                    a{
                    gap: 15px;
                    margin: 30px 0;
                    color: $palette-white;
                    }
                }
                .address{
                    color: $palette-grey;
                    margin: 30px 0;
                }
                .mobile{
                    margin: 15px 0;
                }
            }
        }
    }
    .footer-container{
        width: 100%;
        border-top: 1px solid $palette-grey;
        padding: 60px 0;
        .copyright{
            font-size: 20px;
            gap: 5px;
            margin: 0 auto;
            color: $palette-grey;
            a{
                color: $palette-white;
            }
            i{
                font-size: 14px;
            }
        }
    }
}
</style>