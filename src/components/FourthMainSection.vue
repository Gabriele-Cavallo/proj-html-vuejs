<script>
    export default{
        name: 'FourthMainSection',
    }
</script>

<template>
    <section>
        <div class="background-gradient d-flex algn-cntr">
            <div class="container">
                <div class="col-60">
                    <h4>Join our mailing list today</h4>
                    <h2>Insider offers & flash sales in your inbox every week.</h2>
                    <i class="fa-solid fa-water"></i>
                    <div class="input-wrapper">
                        <input type="text" placeholder="Insert your email...">
                        <button class="btn">Subscribe</button>
                    </div>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure tempore earum dolorum rem odio harum quidem doloribus facere, pariatur at aliquid incidunt minima? Sed commodi explicabo aperiam eaque repudiandae in.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;
section{
    background-image: url('../assets/img/banner1-2x.jpg');
    min-height: 1000px;
    background-size: cover;
    background-position: right;
    background-repeat: no-repeat;
    .background-gradient{
        min-height: 1000px;
        .col-60{
            width: 60%;
            *{
                margin-bottom: 20px;
            }
            i{
                color: $palette-yellow;
                font-size: 50px;
            }
            h4{
                color: $palette-red;
                font-size: 25px;
            }
            h2{
                color: $palette-white;
                font-size: 60px;
            }
            .input-wrapper{
                input{
                    border-radius: 25px;
                    padding: 15px;
                    border: none;
                    width: 400px;
                    margin-right: 20px;
                }
                button{
                    min-width: 200px;
                }

            }
            p{
                color: $palette-grey;
            }
        }
    }
}
</style>