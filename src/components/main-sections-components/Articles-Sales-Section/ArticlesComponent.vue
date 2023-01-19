<script>
import ArticlesCard from './pseudo-components/ArticlesCard.vue';

export default {
    components: {
        ArticlesCard
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
            </div>
        </article>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
.articles-sales{
    padding: 7rem 0;
    .tools{
                display: flex;
                align-items: center;
                justify-content: space-between;
                margin-bottom: 2rem;
    
                i{
                    font-size: 1rem;
                    padding-left: 0.2rem;
                }
            }
            .grid-videos{
                display: flex;
                justify-content: space-between;
                width: 100%;
            }
}
</style>
