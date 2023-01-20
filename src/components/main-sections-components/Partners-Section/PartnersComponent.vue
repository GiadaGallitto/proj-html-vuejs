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
        <article class="partners-cards wrapper-container">
            <!-- Micro component con all'interno i partners da inserire con js -->
            <div class="grid-partners">
                <PartnersCard />
            </div>
        </article>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
.partners{
    width: 100%;
    padding: 7rem 0;
    .partners-cards{
        height: 100%;
        .grid-partners{
            height: 100%;
            width: 100%;
            display: flex;
            justify-content: space-between;
        }
    }
}
</style>
