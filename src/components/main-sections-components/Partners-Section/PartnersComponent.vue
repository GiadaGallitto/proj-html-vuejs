<script>
import PartnersCard from './pseudo-components/PartnersCard.vue';

export default {
    components: {
        PartnersCard,
    }
}
</script>

<template>
    <section class="partners">
        <article class="partners-cards">
            <!-- Micro component con all'interno i partners da inserire con js -->
            <PartnersCard />
        </article>
    </section>
</template>

<style lang="scss" scoped>

</style>
