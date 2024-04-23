<script>
    export default{
        name: 'EighthMainSection',
        data(){
            return{
                services: [
                    {
                        img: 'sponsor-1-2x.png',
                        paragraph: 'Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.',
                        button: 'Visit Yoga Studio',
                    },
                    {
                        img: 'sponsor-2-2x.png',
                        paragraph: 'Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.',
                        button: 'Join Fitness Center',
                    },
                    {
                        img: 'sponsor-3-2x.png',
                        paragraph: 'Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.',
                        button: 'Learn about FC',
                    },
                    {
                        img: 'sponsor-4-2x.png',
                        paragraph: 'Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.',
                        button: 'Visit Power Gym',
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
    <section>
        <div class="container">
            <div class="card-wrapper d-flex jst-btwn">
                <div v-for="service in services" class="card d-flex flex-col algn-cntr">
                    <img :src="getImageUrl(service.img)" alt="service">
                    <i class="fa-solid fa-water"></i>
                    <p>{{ service.paragraph }}</p>
                    <button class="btn d-flex algn-cntr jst-cntr">
                        {{ service.button }}
                        <i class="fa-solid fa-chevron-right"></i>
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;
section{
    padding: 80px 0;
    .container{
        .card-wrapper{
            .card{
                text-align: center;
                padding: 30px;
                width: calc((100% / 4) - 20px);
                p{
                    line-height: 1.5;
                    margin: 20px 0;
                    color: $palette-grey;
                }
                .fa-water{
                    color: $palette-blue;
                    margin: 20px 0;
                }
                .btn{
                    background-color: transparent;
                    color: $palette-black;
                    gap: 10px;
                    font-weight: 600;
                    .fa-chevron-right{
                        font-size: 12px;
                    }
                }
            }
        }
    }
}

</style>