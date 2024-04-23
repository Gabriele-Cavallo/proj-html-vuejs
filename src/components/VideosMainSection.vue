<script>
    export default{
        name: 'VideosMainSection',
        data(){
            return{
                playlist: [
                    {
                        image: 'video2-2x.jpg',
                        title: 'Thighs & glute workout',
                        subTitle: 'Increase your mobility',
                    },
                    {
                        image: 'video7-2x.jpg',
                        title: 'Lift, firm & perk up',
                        subTitle: 'Feel young again',
                    },
                    {
                        image: 'video9-2x.jpg',
                        title: 'Slim & trim your waist',
                        subTitle: 'Shed those extra pounds',
                    },
                ]
            }
        },
        methods: {
            getImageUrl(name) {
                return new URL(`../assets/img/${name}`, import.meta.url).href;
            }
        },
    }
</script>

<template>
    <section id="videos">
        <div class="row">
            <!-- Left column -->
            <div class="col-50 service">
                <div class="img-wrapper anchor">
                    <img src="../assets/img/service15-2x.jpg" alt="service">
                    <button class="play">
                        <i class="fa-solid fa-play"></i>
                    </button>
                </div>
            </div>
            <!-- /Left column -->

            <!-- Right column -->
            <div class="col-50 advice">
                <h4>Tune up your Workouts</h4>
                <h2>The best health & fitness advice online</h2>
                <!-- YouTube references -->
                <div class="youtube-wrapper">
                    <div class="btn-wrapper d-flex algn-cntr">
                        <img src="../assets/img/unnamed.jpg" alt="alt-logo">
                        <div class="youtube-channel">
                            <div class="grey">Theme Fusion</div>
                            <button class="d-flex algn-cntr">
                                <div class="w-70 d-flex algn-cntr jst-cntr">
                                    <i class="fa-brands fa-youtube"></i>
                                    <div >YouTube</div>
                                </div>
                                <span class="w-30 grey">999+</span>
                            </button>
                        </div>
                    </div>
                    <p class="grey">Arcu eu facilist ut quisque pacerat nunc habitant. Magna semper mauris, venenatis,leo integer sit pellentesque.</p>
                    <button class="btn btn-red">
                        <i class="fa-brands fa-youtube"></i>
                        <span>Visit my YouTube channel</span>
                    </button>
                </div>
                <!-- /YouTube references -->
            </div>
            <!-- /Right column -->

            <!-- Videos wrapper -->
            <div class="container anchor">
                <h3>FeaturedPlaylists</h3>
                <div class="video-wrapper d-flex jst-btwn">
                    <!-- Single video box template -->
                    <div v-for="video in playlist"  class="single-video-box">
                        <div class="video-box anchor">
                            <img :src="getImageUrl(video.image)" alt="video playlist">
                            <button class="play">
                                <i class="fa-solid fa-play"></i>
                            </button>
                        </div>
                        <h3>{{ video.title }}</h3>
                        <h4>{{ video.subTitle }}</h4>
                    </div>
                    <!-- /Single video box template -->
                    <a class="d-flex algn-cntr" href="#">View all videos
                        <i class="fa-solid fa-chevron-right"></i>
                    </a>
                </div>
            </div>
            <!-- /Videos wrapper -->
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

section{
    padding-bottom: 200px;
}
.row{
    .col-50{
        width: 50%;
        &.service{
            .img-wrapper{
                height: 870px;  
                position: relative;
                bottom: 50px;
                max-width: 940px;
                border-bottom-right-radius: 35px;
                overflow: hidden;
                &::after{
                    content: '';
                    position: absolute;
                    top: 0;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    background-color: rgba(0, 0, 0, 0.2);
                }
                img{
                    height: 100%;
                    width: 100%;
                }
                button{
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                }
            }
        }
        &.advice{
            padding-left: 40px;
            margin-top: 150px;
            *{
                margin-bottom: 30px;
            }
            h4{
                color: $palette-blue;
                font-size: 25px;
            }
            h2{
                font-size: 65px;
                width: 70%;
            }
            .youtube-wrapper{
                .grey{
                    color: #524a59;
                }
                .btn-wrapper{
                    margin-bottom: 0;
                    img{
                    height: 60px;
                    }
                    .youtube-channel{
                        margin-left: 10px;
                        *{
                            margin-bottom: 5px;
                        }
                        button{
                            background: transparent;
                            border: 1px solid $palette-grey;
                        }
                        .w-70{
                            width: 70%;
                            background-color: #e62117;
                            color: $palette-white;
                            height: 100%;
                            margin-bottom: 0;
                            padding: 5px;
                            gap: 10px;
                            *{
                                margin-bottom: 0;
                            }
                        }
                        .w-30{
                            width: 30%;
                            background-color: $palette-white;
                            height: 100%;
                            margin-bottom: 0;
                            padding: 5px;
                            *{
                                margin-bottom: 0;
                            }
                        }
                    }
                }
                .btn-red{
                    background-color: red;
                    *{
                        margin-bottom: 0;
                        margin-right: 10px;
                    }
                }
            }
        }
    }
    .container{
        h3{
            font-size: 25px;
            margin-top: 60px;
            font-weight: 500;
        }
        .video-wrapper{
            margin-top: 40px;
            .single-video-box{
                width: calc((100% / 3) - 40px);
                text-align: center;
                .video-box{
                border-radius: 5px;
                border-bottom-right-radius: 25px;
                overflow: hidden;
                max-height: 340px;
                    img{
                        height: 100%;
                        width: 100%;
                    }
                    button{
                        position: absolute;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50% , -50%);
                    }
                }
                h3{
                    margin-top: 15px;
                    font-size: 25px;
                }
                h4{
                    color: $palette-blue;
                    margin-top: 15px;
                    font-size: 18px;
                    font-weight: 500;
                }
            }
        }
        a{
            position: absolute;
            top: 50px;
            right: 40px;
            color: black;
            font-weight: 400;
            font-size: 18px;
            gap: 20px;
            i{
                font-size: 14px;
            }
        }
    }
}

</style>