<script>
export default{
    components: {
    },

    data(){
        return {
            videoList: [
                {
                    image: 'blog4-2x-400x258',
                    title: "The best protein shake",
                    admin: "admin",
                },
                {
                    image: 'blog1-2x-400x258',
                    title: "Lift, firm & perk up",
                    admin: "admin",
                },
                {
                    image: 'blog3-2x-400x258',
                    title: "Slim & trim your waist",
                    admin: "admin",
                },
            ],
        };
    },

    methods: {
        getImagePath: function(img){
            return new URL(`../../../../assets/main-imgs/articles-section/${img}.jpg`, import.meta.url).href;
        },
    },
}
</script>

<template>
    <div v-for="videoEl in videoList" class="video-card">
        <div class="image-bg">
            <div class="layover"></div>
            <img :src="getImagePath(videoEl.image)" alt="video image">
        </div>

        <div class="text">
            <a href=""><h6 class="title">{{ videoEl.title }}</h6></a>
            <h5 class="subtitle">By <span><a href="">{{ videoEl.admin }}</a></span> | November 26th, 2019 | <span><a href="">Gym</a></span></h5>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../../../../styles/partials/variables.scss" as *;
.video-card{
    width: calc((100% / 3) - 2rem);
    position: relative;
    .image-bg{
        cursor: pointer;
        width: 100%;
        border-radius: 1% 1% 10% 1%;
        overflow: hidden;
        margin-bottom: 1.5rem;
        position: relative;
        .layover{
            width: 100%;
            height: 100%;
            position: absolute;
            background: linear-gradient(transparent 45%, $DodgerBlueColor);
            opacity: 0;
            transition: all 0.4s ease-in-out;

            &:hover{
                opacity: 0.7;
            };
        };

        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        };
    };
    .text{
        position: relative;
        padding-left: 5%;
        .title{
            color: $CinderColor;
            font-size: 1.4rem;
            font-weight: 600;
            &:hover{
                color: $DodgerBlueColor;
            };
        };
        .subtitle{
            color: $JumboColor;
            font-size: 1rem;
            font-weight: 400;
            span a{
                color: black;
                &:hover{
                color: $DodgerBlueColor;
                };
            };
        };
    };
};
</style>