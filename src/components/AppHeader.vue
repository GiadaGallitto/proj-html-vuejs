<script>
export default {

}
</script>

<template>
    <div class="header-container">
        <!-- Qui inserirò il la barra nera che conterrà logo e nav-bar -->
        <div class="upper-bar wrapper-container">
            <div class="logo w-25">
                <img src="../assets/logo.png" alt="">
            </div>
            <ul class="nav-bar">
                <li>Home</li>
                <li>Services</li>
                <li>About</li>
                <li>Videos</li>
                <li>Blog</li>
                <li>
                    Store
                    <span id="new-btn">new</span>
                </li>
                <li>
                    <button class="blue-btn">Schedule a workout</button>
                </li>
                <li><i class="fa-solid fa-cart-shopping"></i></li>
                <li><i class="fa-solid fa-magnifying-glass"></i></li>
            </ul>
        </div>
        <!-- Qui inserirò il jumbotron con background-image e il container di testo a sinisra del jumbo (va aggiunto anche il componentPlayButton) -->
        <div class="jumbotron">
            <div class="jumbo-text">
                <h4 class="red-title">Certified fitness professional</h4>
                <h1>Take control of your health</h1>
                <!-- Component divider -->
                <div>Divisore</div>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ex in nulla iusto dolorum natus.</p>
                <button class="blue-btn">
                    <i class="fa-brands fa-youtube pe-2 fs-6"></i>
                    Visit my Youtube channel
                </button>
                <button id="empty-btn">
                    Buy Avada today
                    <i class="fa-solid fa-arrow-right"></i>
                </button>
            </div>
            <div class="jumbo-image">
            </div>
            <!-- Component Play Button -->
            <div class="jumbo-details">
                <!-- Elementi di dettaglio a destra del jumbotron -->
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables.scss" as *;

.header-container {
    background-color: $CodGrayColor;

    .upper-bar {
        height: 100%;
        padding: 1.8rem 0;
        justify-content: space-between;
        display: flex;
        align-items: center;
        .nav-bar {
            list-style-type: none;
            margin-bottom: 0;

            li {
                display: inline-block;
                color: $SilverColor;
                padding: 0 1.2rem;
                #new-btn{
                    font-size: 0.9rem;
                    margin-left: 0.6rem;
                    padding: 0.4rem 0.6rem;
                    color: black;
                    background-color: #fff941;
                    border-radius: 2px;
                }
                i{
                    color: $SilverColor;
                    font-size: 1.2rem;
                }
            }
        }
    }

    .jumbotron{
        height: 600px;
        position: relative;
        display: flex;
        justify-content: end;
        .jumbo-text{
            position: absolute;
            top: 0;
            left: 13%;
            z-index: 1;
            padding: 6rem 0 9rem;
            h1{
                color: $WhiteColor;
                padding: 0.5rem 0;
                font-size: 3.5rem;
            };

            p{
                color: $JumboColor;
                padding: 1rem 0;
                font-weight: 500;
            };

            #empty-btn{
                margin-left: 1rem;
                background: none;
                color: $WhiteColor;
                border-color: $JumboColor;
                padding: 0.7rem 2rem;
                border-radius: 25px;
                i{
                    padding-left: 0.5rem;
                    color: $WhiteColor;
                    font-size: 1.2rem;
                    vertical-align: middle;
                }
            }
        };
        // linear-gradient(to bottom, transparent 0%, black 100%);
        .jumbo-image{
            height: 100%;
            width: 100%;
            background-image: linear-gradient(to right, black, black, transparent 70%),
            url("../assets/header-imgs/slider82x-scaled.jpg");
            background-size: 100%;
            background-repeat: no-repeat;
            background-position: top;
        }
    }
}


// Ogni wrapper container all'interno dei components principali avrà una width fissa
</style>
