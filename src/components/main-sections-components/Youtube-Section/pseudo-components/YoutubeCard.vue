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
            <img :src="getImagePath(videoEl.image)" alt="video image">
        </div>
        <div class="text">
            <h3 class="title">{{ videoEl.title }}</h3>
            <h5 class="subtitle">{{ videoEl.subtitle }}</h5>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../../../../styles/partials/variables.scss" as *;
.video-card{
    width: calc((100% / 3) - 2rem);
    position: relative;
    border-radius: 1% 1% 10% 1%;
    overflow: hidden;
    .image-bg{
        width: 100%;
        height: 100%;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .text{
        position: absolute;
        bottom: 7%;
        left: 10%;

        #gray-divider{
            color: $WhiteColor;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }
        .title{
            color: $WhiteColor;
            font-size: 2.2rem;
            line-height: 1.7rem;
        }
        .subtitle{
            color: $YellowColor;
            font-size: 1.4rem;
        }
    }
}
</style>

