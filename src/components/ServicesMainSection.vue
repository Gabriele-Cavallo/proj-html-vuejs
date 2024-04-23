<script>
    export default{
        name: 'ServicesMainSection',
        data (){
            return{
                services: [
                    {
                        image: 'service6-2x.jpg',
                        title: 'Crossfit workout',
                        subTitle: 'Push your limits'
                    },
                    {
                        image: 'box1-2x.jpg',
                        title: 'New gym apparel',
                        subTitle: 'Look good, feel good'
                    },
                    {
                        image: 'box3-2x.jpg',
                        title: 'Team training',
                        subTitle: 'Find a partner'
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
    <section id="services">
        <div class="container">
            <div class="box-wrapper d-flex jst-btwn">
                <div v-for="service in services" class="box anchor d-flex pointer">
                    <img :src="getImageUrl(service.image)" :alt="service.title">
                    <div class="box-title">
                        <i class="fa-solid fa-water"></i>
                        <h3>{{  service.title  }}</h3>
                        <h4>{{  service.subTitle  }}</h4>
                    </div>
                </div>
            </div>
            <div class="sub-container">
                <h2>"How you respond to the challenge in the second half will determine what you become after the game, wheter you are a winner or a loser."</h2>
                <i class="fa-solid fa-water"></i>
                <div class="testimonials d-flex jst-cntr algn-cntr">
                    <img src="../assets/img/avatar-1-2x.jpg" alt="avatar">
                    <div>Brad Johgnson</div>
                    <span>Las Vegas</span>
                </div>
            </div>
        </div>
    </section>

</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;
section{
    background: linear-gradient(135deg, blue, red );
    min-height: 900px;
    padding-bottom: 100px;
    .container{
        .box-wrapper{
            position: relative;
            bottom: 80px;
            .box{
               max-height: 560px;
               width: calc((100% / 3) - 40px);
               border-radius: 5px;
               border-bottom-right-radius: 50px;
               overflow: hidden;
               margin-bottom: 100px;
               transition: all 1s ease;
               &:hover{
                transform: scale(1.1);
               }
               &::after{
                content: '';
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: linear-gradient(to top, rgba(0, 0, 0, 0.4)20%, rgba(0, 0, 0, 0.1)100% );
               }
               img{
                height: 100%;
                width: 100%;
               }
               .box-title{
                position: absolute;
                left: 30px;
                bottom: 40px;
                color: $palette-white;
                    *{
                        margin-top: 10px;
                    }
                    h3{
                        font-size: 30px;
                        text-shadow: 1px 1px 2px black;
                    }
                    h4{
                        font-size: 25px;
                        color: $palette-yellow;
                        text-shadow: 1px 1px 2px black;
                    }
                    i{
                        text-shadow: 1px 1px 2px black;
                    }
                }
            }
        }
        .sub-container{
            width: 80%;
            margin: 0 auto;
            text-align: center;
            color: $palette-white;
            *{
                margin-bottom: 15px;
            }
            i{
                font-size: 50px;
                color: $palette-yellow;
            }
            h2{
                font-size: 40px;
            }
            .testimonials{
                gap: 20px;
                img{
                    border-radius: 50%;
                    transform: scale(0.75);
                }
                div{
                    font-weight: bold;
                    font-size: 20px;
                }
                span{
                    color: $palette-grey;
                    font-size: 20px;
                }
            }
        }
    }
}
</style>