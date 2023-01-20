<script>
import PlayButtonComponent from '../../PlayButtonComponent.vue';

export default {
    components: {
        PlayButtonComponent,
    }
}
</script>

<template>
    <section class="daily-workout">
        <article class="work-jumbo">
            <PlayButtonComponent class="play-work" />
            <div class="info-workout">
                <h1>Crossfit workout of the day</h1>
                <h3>November 15th, 2019</h3>
                <p><a href="">View all videos <i class="fa-solid fa-arrow-right-long"></i></a></p>
            </div>
        </article>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
.daily-workout{
    width: 100%;
    .work-jumbo {
        height: 650px;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top: 10rem;
        background-image:linear-gradient(108deg, rgba(33, 15, 139, 0.5) 5%, rgba(29, 12, 122, 0.5) 17%, rgba(29, 16, 105, 0.5) 35%, rgba(59, 7, 94, 0.5) 47%, rgba(117, 22, 56, 0.5) 77%, rgba(146, 32, 53, 0.5) 92%, rgba(128, 32, 37, 0.5) 100%),
            url("../../../assets/main-imgs/workout-section/banner14-2x.jpg");
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        position: relative;
        .play-work{
            top: 25%;
            left: 46%;
        };
        .info-workout {
            width: 35%;
            text-align: center;
            color: $WhiteColor;

            h1 {
                font-size: 3.7rem;
                margin-bottom: 2rem;
            };

            h3{
                font-size: 2.5rem;
                color: $YellowColor;
                margin-bottom: 1rem;
            };

            p a{
                color: $WhiteColor;
                font-size: 1.2rem;
                margin-bottom: 2rem;
                i {
                    margin-left: 0.2rem;
                };
            };
        };
    };
};
</style>