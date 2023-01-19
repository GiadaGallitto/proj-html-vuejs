<script>
export default{
    components: {
    },

    data(){
        return {
            videoList: [
                {
                    image: 'video2-2x',
                    title: "Thighs & glue workout",
                    subtitle: "Increase your mobility"
                },
                {
                    image: 'video7-2x',
                    title: "Lift, firm & perk up",
                    subtitle: "Feel young again"
                },
                {
                    image: 'video9-2x',
                    title: "Slim & trim your waist",
                    subtitle: "Shed those extra pounds"
                },
            ]
        }
    },

    methods: {
        getImagePath: function(img){
            return new URL(`../../../../assets/main-imgs/youtube-section/${img}.jpg`, import.meta.url).href;
        },
    }
}
</script>

<template>
    <div v-for="videoEl in videoList" class="video-card">
        <div class="image-bg">
            <div class="playlist-play"><i class="fa-solid fa-play"></i></div>
            <img :src="getImagePath(videoEl.image)" alt="video image">
        </div>
        <div class="text">
            <h6 class="title">{{ videoEl.title }}</h6>
            <h5 class="subtitle">{{ videoEl.subtitle }}</h5>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../../../../styles/partials/variables.scss" as *;
.video-card{
    width: calc((100% / 3) - 2rem);
    position: relative;
    .image-bg{
        width: 100%;
        border-radius: 1% 1% 10% 1%;
        overflow: hidden;
        margin-bottom: 1.5rem;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        };
        .playlist-play{
            position: absolute;
            top: 30%;
            left: 41%;
            // transform: translate(-50% , -50%);
            color: $DodgerBlueColor;
            background-color: $WhiteColor;
            padding: 1.4rem 1.7rem;
            border-radius: 50%;
            font-size: 0.8rem;
        }
    }
    .text{
        position: relative;
        text-align: center;
        .title{
            color: $CinderColor;
            font-size: 1.3rem;
        }
        .subtitle{
            color: $DodgerBlueColor;
            font-size: 1rem;
        }
    }
}
</style>

