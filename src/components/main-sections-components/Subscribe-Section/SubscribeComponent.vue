<script>
import CourseCard from './pseudo-components/CourseCard.vue';

export default {
    components: {
        CourseCard,
    }
}
</script>

<template>
    <section class="fitness-subscribes">
        <article class="upper-sub">
            <!-- Mini jumbo con background-image -->
            <div class="sub-infos">
                <!-- Contenitore di testo a sinistra con info per il subscribe -->
            </div>
        </article>
        <article class="types-courses">
            <!-- Micro component con all'interno alcuni dei corsi da inserire con js -->
            <CourseCard />
        </article>
    </section>
</template>

<style lang="scss" scoped>

</style>
