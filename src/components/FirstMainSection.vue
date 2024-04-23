<script>
    export default{
        name: 'FirstMainSection',

        data(){
            return{

            }
        }
    }
</script>

<template>
    <section class="anchor">
        <div class="background-gradient">
            <div class="container d-flex algn-cntr">
                <div class="left-col">
                    <h4>Certified fitness professional</h4>
                    <h2>Take control of your health</h2>
                    <i class="fa-solid fa-water"></i>
                    <small>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.</small>
                    <div class="btn-wrapper">
                        <button class="btn hover-red">
                            <i class="fa-brands fa-youtube"></i>
                            <span>Visit my YouTubeChannel</span>
                        </button>
                        <button class="btn btn-black">
                            <span>Buy Avada today</span>
                            <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </div>
                <div class="right-col d-flex jst-cntr algn-cntr">
                    <button class="play">
                        <i class="fa-solid fa-play"></i>
                    </button>
                    <div class="anchor-btn d-flex flex-col">
                        <button class="square-white d-flex flex-col algn-cntr jst-cntr">
                            <i class="fa-solid fa-folder"></i>
                            <span>Demos</span>
                        </button>
                        <button class="square-white d-flex flex-col algn-cntr jst-cntr">
                            <div>
                                <div class="price anchor">39
                                    <span>$</span>
                                </div>
                            </div>
                            <span>On Sale</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

section{
    color: $palette-white;
    min-height: 900px;
    background-image: url('../assets/img/slider82x-scaled.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: top;
    .background-gradient{
        .container {
            min-height: 900px;
            .left-col{
                width: 50%;
                display: flex;
                flex-direction: column;
                gap: 40px;
                .fa-water{
                color: $palette-yellow;
                }
                h4{
                    color: $palette-red;
                    font-size: 25px;
                }
                h2{
                    font-size: 60px;
                }
                small{
                    color: $palette-grey;
                    font-size: 16px;
                }
                .btn-wrapper button{
                    margin-bottom: 15px;
                    margin-right: 10px;
                    &.btn *{
                        margin-right: 10px;
                    }
                    &.btn-black{
                        background-color: $palette-black;
                        border: 1px solid $palette-grey;
                    }
                }
            }
            .right-col{
                width: 50%;
                .play{
                    height: 120px;
                    width: 120px;
                    i{
                        font-size: 30px;
                    }
                }
                .anchor-btn{
                    position: absolute;
                    right: 20px;
                    top: 50px;
                    .square-white{
                        margin-bottom: 5px;
                        span{
                            font-weight: bold;
                        }
                        i{
                            font-size: 30px;
                            margin-bottom: 10px;
                        }
                        .price{
                            color: #83bf7b;
                            font-size: 30px;
                            font-weight: bold;
                            margin-bottom: 5px;
                            span{
                                position: absolute;
                                top: 0;
                                left: -10px;
                                font-size: 18px;
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>