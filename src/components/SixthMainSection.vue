<script>
    export default{
        name: 'SixthMainSection',
        data(){
            return{
                playlist: [
                    {
                        image: 'blog4-2x.jpg',
                        title: 'The best protein shake',
                        subTitle: 'By admin | November 26th, 2019 | Gym',
                    },
                    {
                        image: 'blog1-2x.jpg',
                        title: 'Ultimate cardio workout',
                        subTitle: 'By admin | November 26th, 2019 | Gym',
                    },
                    {
                        image: 'blog3-2x.jpg',
                        title: 'New juices available now',
                        subTitle: 'By admin | November 26th, 2019 | Gym',
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
        <div class="container anchor">
            <h3>Latest articles</h3>
            <div class="blog-wrapper d-flex jst-btwn">
                <div v-for="video in playlist"  class="single-blog-box">
                    <img :src="getImageUrl(video.image)" alt="video playlist">
                    <h3>{{ video.title }}</h3>
                    <small>{{ video.subTitle }}</small>
                </div>
                <a class="d-flex algn-cntr" href="#">Read all articles
                    <i class="fa-solid fa-chevron-right"></i>
                </a>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;
section{
    padding: 80px 0;
    .container{
        h3{
            font-size: 25px;
            margin-top: 60px;
            font-weight: 500;
        }
        .blog-wrapper{
            margin-top: 40px;
            .single-blog-box{
                width: calc((100% / 3) - 40px);
                img{
                    height: 340px;
                    width: 100%;
                    cursor: pointer;
                    
                }
                h3{
                    margin-top: 20px;
                    margin-bottom: 15px;
                    font-size: 25px;
                }
                small{
                    color: $palette-grey;
                    font-size: 18px;
                }
            }
        }
        a{
            position: absolute;
            top: 0;
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