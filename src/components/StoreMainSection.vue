<script>
    export default{
        name: 'StoreMainSection',
    }
</script>

<template>
    <section id="store">
        <div class="background-gradient-bottom d-flex jst-cntr algn-cntr">
            <div class="container">
                <h2>"I've failed over and over again in my life. And that is why I succeed."</h2>
                <div class="d-flex jst-cntr"><i class="fa-solid fa-water"></i></div>
                <p>Arcu auctor gravida nisl, congue sit nisi tincidunt eget proin. In lacinia lacus donec sed massa in ipsum ero, tristique. Gravida suspendisse etiam in iaculis</p>
                <div class="btn-wrapper d-flex jst-cntr algn-cntr">
                    <button class="btn">Buy Avada today
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
    background-image: url('../assets/img/banner2-2x.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 900px;
    color: $palette-white;
    text-align: center;
    .background-gradient-bottom{
        background: linear-gradient(to top, #060607, rgba(0, 0, 0, 0.1) 100%);
        min-height: 900px;
        .container{
            width: 50%;
            h2{
                font-size: 60px;
                margin-bottom: 20px;
            }
            .fa-water{
                color: $palette-yellow;
            }
            p{
                margin: 30px;
            }
            button{
                i{
                    font-size: 12px;
                }
            }
        }
    }
}
</style>