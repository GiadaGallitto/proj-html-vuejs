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
        <article class="latest-articles">
            <!-- Micro component con all'interno alcuni degli ultimi articoli da inserire con js -->
            <ArticlesCard />
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

</style>
