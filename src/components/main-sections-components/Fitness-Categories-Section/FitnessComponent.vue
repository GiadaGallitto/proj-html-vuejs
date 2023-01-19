<script>
import CategoriesCard from './pseudo-components/CategoriesCard.vue';
import DividerComponent from '../../DividerComponent.vue';

export default {
    components: {
        CategoriesCard,
        DividerComponent,
    }
}
</script>

<template>
    <section class="fitness-categories">
        <div class="wrapper-container">
            <!-- Micro component con all'interno le categorie di fitness mostrate con js -->
            <article class="grid-categories">
                <CategoriesCard />
            </article>

            <article class="quote">
                <!-- Contenitore di testo con citazione, divider e nome/luogo della persona (per la struttura di questo -> classe e modifica unica per tutte le simili) -->
                <h1>"How you respond to the challenge in the second half will determine what you become after the game, whether you are a winner or a loser."</h1>
                <DividerComponent id="yellow-divider" />
                <div class="author">
                    <div class="img-author"></div>
                    <div id="name-author">Brad Johnson</div>
                    <div id="place-author">Las Vegas</div>
                </div>
            </article>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
    .fitness-categories{
        background-color: rgb(12, 94, 66);
        height: 900px;
        position: relative;
        .grid-categories{
            position: relative;
            top: -11%;
            display: flex;
            justify-content: space-between;
            width: 100%;
        };
        .quote{
            width: 62%;
            margin: 1.5rem auto;
            text-align: center;
            color: $WhiteColor;

            #yellow-divider{
                color: $YellowColor;
                font-size: 1.3rem;
                line-height: 3rem;
            };
            .author{
                display: flex;
                align-items: center;
                justify-content: center;

                div{
                    margin-right: 1.5rem;
                    font-size: 1.4rem;
                    &.img-author{
                        border-radius: 50%;
                        overflow: hidden;
                        width: 70px;
                        height: 70px;
                        background-image: url("../../../assets/main-imgs/fitness-section/avatar-1-2x.jpg");
                        background-size: contain;
                    };

                    &#name-author{
                        font-weight: 500;
                    };

                    &#place-author{
                        color: $SilverColor;
                    }
                }
            }
        }
    }
</style>
