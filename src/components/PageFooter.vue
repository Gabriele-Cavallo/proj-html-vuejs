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
        }
    }
</script>

<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-33">
                    <img class="footer-logo" src="../assets/img/logo-2x.png" alt="logo">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, provident? Nemo dolore impedit nostrum animi soluta itaque at beatae, sequi molestiae cupiditate eaque fugit, corrupti minus id sint ipsa labore.</p>
                    <div class="social-wrapper">
                        <i v-for="social in footerInfo.socialLinks" :class="social.social"></i>
                    </div>
                </div>
                <div class="col-33">
                    <h3>RECENT POST</h3>
                    <ul>
                        <li v-for="post in footerInfo.posts">
                            <a class="d-flex jst-cntr" href="#">
                                <i class="fa-solid fa-chevron-right"></i>
                                <div class="post">{{ post.link }}</div>
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-33">
                    <h3>CONTACT INFORMATION</h3>
                    <div class="address">{{ footerInfo.contacts[0].address }}</div>
                    <div class="mobile">{{ footerInfo.contacts[0].mobile }}</div>
                    <div>{{ footerInfo.contacts[0].email }}</div>
                </div>
            </div>
        </div>
        <div class="footer-container">
            <div class="copyright d-flex jst-cntr algn-cntr">
                <i></i>
                <div>Copyright 2012 - 2020 | Avada theme by</div>
                <a href="#">Theme Fusion</a>
                <div> | All rights reserved | Powered by </div>
                <a href="#">WordPress</a>
            </div>
        </div>
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
        }
    }
}
</style>