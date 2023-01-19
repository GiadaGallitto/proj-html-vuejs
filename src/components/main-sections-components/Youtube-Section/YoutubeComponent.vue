<script>
import YoutubeCard from './pseudo-components/YoutubeCard.vue';
import PlayButtonComponent from '../../PlayButtonComponent.vue';

export default {
    components: {
        YoutubeCard,
        PlayButtonComponent,
    }
}
</script>

<template>
    <section class="youtube-features">
        <article class="main-youtube flex-container">
            <div class="main-video">
                <!-- Immagine e Component Play Button -->
                <PlayButtonComponent class="youtube-play" />
            </div>
            <div class="youtube-infos">
                <!-- Testo con info canale youtube e button -->
            </div>
        </article>

        <article class="features-youtube wrapper-container">
            <!-- Micro component con all'interno alcuni dei video da inserire con js -->
            <YoutubeCard />
        </article>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
.youtube-features{
    height: 900px;
    position: relative;
    .main-youtube{
        position: relative;
        display: flex;
        height: 750px;
        .main-video{
            width: 50%;
            height: 100%;
            background-image: url("../../../assets/main-imgs/youtube-section/service15-2x.jpg");
            background-size: cover;
            border-radius: 0% 1% 5% 0%;
            overflow: hidden;
            position: absolute;
            left: 0;
            top: -7%;
            .youtube-play{
                top: 50%;
                left: 50%;
                transform: translate(-50% , -50%);
            }
        }
    }
}
</style>
