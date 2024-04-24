<script>
    export default{
        name: 'BlogMainSection',
        data(){
            return{
                playlist: [
                    {
                        image: 'blog4-2x.jpg',
                        title: 'The best protein shake',
                    },
                    {
                        image: 'blog1-2x.jpg',
                        title: 'Ultimate cardio workout',
                    },
                    {
                        image: 'blog3-2x.jpg',
                        title: 'New juices available now',
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
    <section id="blog">
        <div class="container anchor">
            <h3>Latest articles</h3>
            <!-- Blogs wrapper -->
            <div class="blog-wrapper d-flex jst-btwn">
                <!-- Single blog box template -->
                <div v-for="video in playlist"  class="single-blog-box">
                    <div class="img-gradient anchor">
                        <img :src="getImageUrl(video.image)" alt="video playlist">
                    </div>
                    <h3>{{ video.title }}</h3>
                    <small class="d-flex algn-cntr small-link">
                        By 
                        <a href="#">admin</a> 
                        | November 26th, 2019 | 
                        <a href="#">Gym</a>
                    </small>
                </div>
                <!-- /Single blog box template -->
                <a class="d-flex algn-cntr" href="#">Read all articles
                    <i class="fa-solid fa-chevron-right"></i>
                </a>
            </div>
            <!-- /Blogs wrapper -->
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
                cursor: pointer;
                &:hover .img-gradient{
                    &::after{
                        content: '';
                        position: absolute;
                        top: 0;
                        left: 0;
                        right: 0;
                        bottom: 0;
                        background: linear-gradient(to top, rgba(0, 8, 255, 0.3)5%, rgba(0, 8, 255, 0)100%);
                    }
                }
                img{
                    max-height: 340px;
                    width: 100%;
                    display: block;
                }
                h3{
                    margin-top: 20px;
                    margin-bottom: 15px;
                    font-size: 25px;
                }
                small{
                    color: $palette-grey;
                    font-size: 18px;
                    gap: 5px;
                    &.small-link{
                        a{
                        position: relative;
                        right: 0;
                        }
                    }
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