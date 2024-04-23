<script>
    export default{
        name: 'FifthMainSection',
        data(){
            return{
                cards:[
                    {
                        icon: 'fa-solid fa-people-group',
                        title: 'Team training',
                        subTitle: 'Find a partner',
                        paragraph: 'Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Misl sit frames amet sectus eget sed duis vehicula. Tristique.',
                        button: 'Find a partner',
                    },
                    {
                        icon: 'fa-solid fa-dumbbell',
                        title: 'Crossfit workout',
                        subTitle: 'Push your limits',
                        paragraph: 'Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Misl sit frames amet sectus eget sed duis vehicula. Tristique.',
                        button: 'Learn about Crossfit',
                    },
                    {
                        icon: 'fa-solid fa-person-running',
                        title: 'Weight loss plan',
                        subTitle: 'Shed those pounds',
                        paragraph: 'Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Misl sit frames amet sectus eget sed duis vehicula. Tristique.',
                        button: 'Schedule a workout',
                    },
                ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="container">
            <div class="card-wrapper d-flex jst-btwn">
                <div v-for="card in cards" class="card">
                    <i :class="card.icon"></i>
                    <h3>{{ card.title }}</h3>
                    <h4>{{ card.subTitle }}</h4>
                    <p>{{ card.paragraph }}</p>
                    <div class="button-wrapper d-flex algn-cntr jst-cntr">
                        <button>{{ card.button }}</button>
                        <i class="fa-solid fa-chevron-right"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;
section{
    padding: 80px 0;
    background-color: $palette-black;
    .container{
        .card-wrapper{
            .card{
                width: calc((100% / 3) - 40px);
                border: 3px solid #3240c1;
                text-align: center;
                color: $palette-white;
                padding: 60px 30px;
                transition: all 1s ease;
                border-radius: 10px;
                h3{
                    margin-top: 40px;
                    margin-bottom: 10px;
                }
                h4{
                    color: $palette-yellow;
                    margin-bottom: 40px;
                }
                p{
                    color: $palette-grey;
                    line-height: 1.5;
                    margin-bottom: 30px;
                }
                i{
                    font-size: 50px;

                    &.fa-dumbbell{
                        transform: rotate(-45deg);
                    }
                }
                .button-wrapper{
                    gap: 15px;
                    button{
                        background: transparent;
                        border: none;
                        font-weight: bold;
                        color: $palette-white;
                    }
                    i{
                        font-size: 10px;
                        font-weight: 900;
                    }
                }
                &:hover{
                    transform: scale(1.1);
                }
            }
        }
    }
}
</style>