<script>
    export default{
        name: 'BottomMainSection',
    }
</script>

<template>
    <section>
        <div class="container d-flex jst-cntr algn-cntr flex-col">
            <button class="play">
                <i class="fa-solid fa-play"></i>
            </button>
            <h2>Crossfit workout of the day</h2>
            <h3>November 15th, 2019</h3>
            <button class="btn-wrapper">
                <!-- Video gallery link -->
                <a href="#" class="d-flex jst-cntr algn-cntr">
                    <div>View all videos</div>
                    <i class="fa-solid fa-arrow-right-long"></i>
                </a>
                <!-- /Video gallery link -->
            </button>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

section{
    background-image: linear-gradient(151deg, $palette-blue 40%, $palette-red 100%), url('../assets/img/banner14-2x.jpg');
    background-blend-mode: multiply;
    background-repeat: repeat;
    background-size: cover;
    background-position: center bottom;
    min-height: 900px;
    .container{
        min-height: 900px;
        width: 50%;
        h2{
            font-size: 60px;
            color: $palette-white;
            margin: 40px 0;
        }
        h3{
            font-size: 45px;
            color: $palette-yellow;
        }
        button{
            height: 120px;
            width: 120px;
            i{
                font-size: 30px;
            }
            &.btn-wrapper{
                min-width: 200px;
                background-color: transparent;
                border: none;
                font-size: 25px;
                a{
                    gap: 15px;
                    color: $palette-white;
                }
                i{
                    font-size: 20px;
                }
            }
        }
    }
}
</style>