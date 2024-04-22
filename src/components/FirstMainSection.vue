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
        <div class="container d-flex algn-cntr">
            <div class="left-col">
                <h4>Certified fitness professional</h4>
                <h2>Take control of your health</h2>
                <span>[wave]</span>
                <small>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.</small>
                <div class="btn-wrapper">
                    <button class="btn">
                        <i>[youtube]</i>
                        <span>Visit my YouTubeChannel</span>
                    </button>
                    <button class="btn btn-black">
                        <span>Buy Avada today</span>
                        <i>[arrow]</i>
                    </button>
                </div>
            </div>
            <div class="right-col">
                <i></i>
                <i></i>
                <i></i>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

section{
    background-color: $palette-black;
    color: $palette-white;
    min-height: 900px;
    background-image: url('../assets/img/slider82x-scaled.jpg');
    object-fit: contain;
    .container {
        min-height: 900px;
        .left-col{
            display: flex;
            flex-direction: column;
            gap: 40px;
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
                margin-right: 10px;
                &.btn-black{
                    background-color: $palette-black;
                    border: 1px solid $palette-grey;
                }
            }
        }
    }
}
</style>