<script>
// Qui verranno importati i macro componenti delle sezioni, ciascuna sezione conterrà a sua volta micro componenti per le schede ripetute
import FitnessComponent from './main-sections-components/Fitness-Categories-Section/FitnessComponent.vue';
import YoutubeComponent from './main-sections-components/Youtube-Section/YoutubeComponent.vue';
import SubscribeComponent from './main-sections-components/Subscribe-Section/SubscribeComponent.vue';
import ArticlesComponent from './main-sections-components/Articles-Sales-Section/ArticlesComponent.vue';
import PartnersComponent from './main-sections-components/Partners-Section/PartnersComponent.vue';
import DailyWorkoutComponent from './main-sections-components/Daily-Workout-Section/DailyWorkoutComponent.vue';

export default{
    components: {
        FitnessComponent,
        YoutubeComponent,
        SubscribeComponent,
        ArticlesComponent,
        PartnersComponent,
        DailyWorkoutComponent
    }
}
</script>

<template>
    <div class="main-container">
        <div class="wrapper-container">
            <FitnessComponent />

            <YoutubeComponent />

            <SubscribeComponent />

            <ArticlesComponent />

            <PartnersComponent />

            <DailyWorkoutComponent />
        </div>
    </div>
</template>

<style lang="scss">

</style>
