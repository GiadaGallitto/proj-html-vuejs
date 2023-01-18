<script>
import CategoriesCard from './pseudo-components/CategoriesCard.vue';

export default {
    components: {
        CategoriesCard,
    }
}
</script>

<template>
    <section class="fitness-categories">
        <!-- Micro component con all'interno le categorie di fitness mostrate con js -->
        <CategoriesCard />
        <div class="quote">
            <!-- Contenitore di testo con citazione, divider e nome/luogo della persona (per la struttura di questo -> classe e modifica unica per tutte le simili) -->
        </div>
    </section>
</template>

<style lang="scss" scoped>

</style>
