<script>
import PlayButtonComponent from './PlayButtonComponent.vue';
import DividerComponent from './DividerComponent.vue';

export default {
    components: {
        PlayButtonComponent,
        DividerComponent,
    }
}
</script>

<template>
    <div class="header-container">
        <div class="upper-bar wrapper-container">
            <div class="logo w-25">
                <img src="../assets/logo.png" alt="">
            </div>
            <ul class="nav-bar">
                <li><a href="">Home</a></li>
                <li><a href="">Services</a></li>
                <li><a href="">About</a></li>
                <li><a href="">Videos</a></li>
                <li><a href="">Blog</a></li>
                <li>
                    <a href="">Store</a>
                    <span id="new-btn">new</span>
                </li>
                <li><button class="blue-btn">Schedule a workout</button></li>
                <li><a href=""><i class="fa-solid fa-cart-shopping"></i></a></li>
                <li><a href=""><i class="fa-solid fa-magnifying-glass"></i></a></li>
            </ul>
        </div>

        <div class="jumbotron">
            <div class="jumbo-text">
                <h4 class="red-title">Certified fitness professional</h4>
                <h1>Take control of your health</h1>
                <DividerComponent id="yellow-divider" />
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

            <div class="jumbo-image"></div>

            <PlayButtonComponent class="header-play" />
            <div class="jumbo-details">
                <div class="box-detail">
                    <i class="fa-solid fa-download"></i>
                    <span class="d-block">Demos</span>
                </div>
                <div class="box-detail">
                    <i class="fa-solid fa-dollar-sign" id="green-icon"></i>
                    <span class="d-block">On Sale</span>
                </div>
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
                padding: 0 1.2rem;
                font-size: 1.1rem;
                a{                    
                    color: $SilverColor;
                    transition: all 0.2s ease-in;
                    &:hover{
                        color: $WhiteColor;
                    };
                };

                #new-btn{
                    font-size: 0.9rem;
                    font-weight: 400;
                    margin-left: 0.6rem;
                    padding: 0.45rem 0.6rem 0.4rem;
                    color: black;
                    background-color: $YellowColor;
                    border-radius: 2px;
                };

                i{
                    color: $SilverColor;
                    font-size: 1.2rem;
                    transition: all 0.2s ease-in;
                    &:hover{
                        color: $WhiteColor;
                    };
                };
            };
        };
    };

    .jumbotron{
        height: 650px;
        position: relative;
        display: flex;
        justify-content: end;
        .jumbo-text{
            position: absolute;
            top: 0;
            left: 15%;
            z-index: 1;
            padding: 8rem 0 7rem;
            h1{
                color: $WhiteColor;
                padding: 0.5rem 0;
                font-size: 3.5rem;
            };

            #yellow-divider{
                color: $YellowColor;
                font-size: 1.2rem;
            };

            p{
                color: $JumboColor;
                padding: 1rem 0;
                font-weight: 500;
                font-size: 1.1rem;
            };

            #empty-btn{
                margin-left: 1rem;
                background: black;
                border: 2px solid $JumboColor;
                color: $WhiteColor;
                font-weight: 500;
                padding: 0.9rem 2rem 0.7rem;
                border-radius: 25px;
                transition: all 0.3s ease-in-out;

                &:hover{
                    border: 2px solid $WhiteColor;
                    background-color: $WhiteColor;
                    color: black;

                    &:hover i{
                        color: black;
                    };
                };

                i{
                    padding-left: 0.5rem;
                    color: $WhiteColor;
                    font-size: 1.2rem;
                    vertical-align: middle;
                    transition: all 0.2s ease-in-out;
                };
            };
        };
        .jumbo-image{
            height: 100%;
            width: 100%;
            background-image: linear-gradient(to right, black, black, black, transparent 60%),
            url("../assets/header-imgs/slider82x-scaled.jpg");
            background-size: 100%;
            background-repeat: no-repeat;
            background-position: top;
        };
        .header-play{
            top: 38%;
            right: 21%;
        }
        .jumbo-details{
            position: absolute;
            top: 8%;
            right: 1%;
            div{
                cursor: pointer;
                background-color: $WhiteColor;
                color: #33475b;
                font-weight: 600;
                text-align: center;
                padding: 0.5rem 1rem;
                margin-bottom: 0.5rem;
                border-radius: 8px;

                i{
                    padding-bottom: 0.5rem;
                    font-size: 2rem;

                    &#green-icon{
                        color: #81c891;
                    };
                };
            };
        };
    };
};
</style>
