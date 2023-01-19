<script>
import ArticlesCard from './pseudo-components/ArticlesCard.vue';
import DividerComponent from '../../DividerComponent.vue';

export default {
    components: {
        ArticlesCard,
        DividerComponent,
    }
}
</script>

<template>
    <section class="articles-sales">
        <article class="latest-articles wrapper-container">
            <!-- Micro component con all'interno alcuni degli ultimi articoli da inserire con js -->
            <div class="tools">
                <h3>Latest articles</h3>
                <h5>
                    Read all articles
                    <i class="fa-solid fa-chevron-right"></i>
                </h5>
            </div>
            <div class="grid-videos">
                <ArticlesCard />
            </div>
        </article>

        <article class="main-sales">
            <!-- Mini jumbo con background-image -->
            <div class="quote-sales">
                <!-- Contenitore di testo al centro con una quote e un button per acquistare -->
                <h1>"I've failed over and over again in my life. And that is why I succeed."</h1>
                <DividerComponent id="yellow-divider" />
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ullam debitis atque enim, exercitationem
                    saepe rem ducimus ad! Esse magni excepturi voluptate optio atque sed tempora?</p>
                <button class="blue-btn" id="buy-btn">Buy Avada today <i class="fa-solid fa-chevron-right"></i></button>
            </div>
        </article>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;

.articles-sales {
    width: 100%;

    .latest-articles {
        padding: 7rem 0;

        .tools {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 2rem;

            i {
                font-size: 1rem;
                padding-left: 0.2rem;
            }
        }

        .grid-videos {
            display: flex;
            justify-content: space-between;
            width: 100%;
        }
    }

    .main-sales {
        height: 600px;
        width: 100%;
        display: flex;
        justify-content: center;
        padding-top: 11rem;
        background-image: linear-gradient(transparent 20%, black),
            url("../../../assets/main-imgs/articles-section/banner2-2x.jpg");
        background-size: cover;
        background-repeat: no-repeat;

        .quote-sales {
            width: 35%;
            text-align: center;
            color: $WhiteColor;

            h1 {
                font-size: 2.8rem;
            };

            #yellow-divider {
                color: $YellowColor;
                font-size: 1.3rem;
                line-height: 3.2rem;
                margin-bottom: 1rem;
            };

            p {
                color: $SilverColor;
                font-size: 1.1rem;
                margin-bottom: 2rem;
            };
            .blue-btn {
                &#buy-btn {
                    padding-top: 0.8rem;
                    font-size: 1.1rem;
                    width: 32%;
                };
                .fa-chevron-right{
                    font-size: 0.8rem;
                    padding-left: 0.5rem
                };
            }
        }
    }
}

;
</style>
