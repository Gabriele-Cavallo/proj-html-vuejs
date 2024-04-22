<script>
    import { store } from '../store.js'
    export default{
        name: 'PageHeader',
        data(){
            return{
                store,
                headerLinks: ['Home', 'Services', 'About', 'Videos', 'Blog', 'Store']
            }
        }
    }
</script>

<template>
    <header>
        <div class="header-wrapper container d-flex jst-btwn algn-cntr">
            <!-- Logo Image -->
            <img src="../assets/img/logo-2x.png" alt="logo">

            <!-- Menu Header -->
            <div class="header-menu-wrapper d-flex algn-cntr">
                <!-- Links navigation -->
                <ul class="nav-bar d-flex">
                    <a v-for="link in headerLinks" href="#">
                        <li>{{link}}</li>
                    </a>
                </ul>
                <span class="badge">new</span>
                <!-- /Links navigation -->

                <!-- Info + Shop + Find Menu -->
                <div class="header-btn-wrapper d-flex algn-cntr">
                    <button class="btn">Schedule a workout</button>
                    <button class="btn-no-style">
                        <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
                    </button>
                    <button class="btn-no-style">
                        <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
                    </button>
                </div>
                <!-- /Info + Shop + Find Menu -->
            </div>
            <!-- /Menu Header -->
        </div>
    </header>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

header{
    background-color: $palette-black;
    height: 100px;
    .header-wrapper{
        height: 100%;
        color: $palette-white;
        img{
            width: 220px;
        }
        .header-menu-wrapper{
            .nav-bar a:hover{
                color: $palette-white;
            }
            ul{
                gap: 40px;
                a{
                    color: $palette-grey;
                    font-size: 25px;
                    font-weight: bold;
                }
            }
            .badge{
                background-color: $palette-yellow;
                color: $palette-black;
                padding: 5px;
                margin-left: 10px;
                border-radius: 5px;
                font-size: 20px;
            }
            .header-btn-wrapper{
                gap: 50px;
                margin-left: 40px;
                .btn{
                    background-color: $palette-blue;
                    border: none;
                    border-radius: 20px;
                    color: $palette-white;
                    padding: 15px 35px;
                    font-weight: bold;
                    cursor: pointer;
                }
                .btn-no-style{
                    background-color: transparent;
                    border: none;
                    i{
                        color: $palette-grey;
                        font-size: 18px;
                    }
                }
            }
        }
}
}
</style>