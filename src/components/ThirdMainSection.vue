<script>
    export default{
        name: 'ThirdMainSection',
    }
</script>

<template>
    <div class="row">
        <div class="col-50 service">
            <div class="img-wrapper anchor">
                <img src="../assets/img/service15-2x.jpg" alt="service">
                <button class="play">
                    <i class="fa-solid fa-play"></i>
                </button>
            </div>
        </div>
        <div class="col-50 advice">
            <h4>Tune up your Workouts</h4>
            <h2>The best health & fitness advice online</h2>
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
        </div>
        <div class="container">
            <h4>FeaturedPlaylists</h4>
            <div class="video-box">
                <button class="play"></button>
            </div>
            <a href="#">View all videos
                [chevron]
            </a>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

.row{
    .col-50{
        width: 50%;
        &.service{
            .img-wrapper{
                height: 870px;  
                position: relative;
                bottom: 50px;
                width: 940px;
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
}

</style>