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
        <div class="wrapper-container">
            <!-- Micro component con all'interno le categorie di fitness mostrate con js -->
            <div class="grid-categories">
                <CategoriesCard />
            </div>
            <div class="quote">
                <!-- Contenitore di testo con citazione, divider e nome/luogo della persona (per la struttura di questo -> classe e modifica unica per tutte le simili) -->
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
    .fitness-categories{
        background-color: aquamarine;
        height: 500px;
        position: relative;
        .grid-categories{
            position: relative;
            top: -23%;
            display: flex;
            justify-content: space-between;
            width: 100%;
        }
    }
</style>
