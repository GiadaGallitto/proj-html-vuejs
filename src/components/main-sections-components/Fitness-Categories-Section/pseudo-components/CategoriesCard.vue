<script>
import DividerComponent from '../../../DividerComponent.vue';

export default{
    components: {
        DividerComponent,
    },

    data(){
        return {
            categoriesList: [
                {
                    image: 'service6-2x',
                    title: "Crossfit workout",
                    subtitle: "Push your limits"
                },
                {
                    image: 'box1-2x',
                    title: "New gym apparel",
                    subtitle: "Look good, feel good"
                },
                {
                    image: 'box3-2x',
                    title: "Team training",
                    subtitle: "Find a partner"
                },
            ]
        }
    },

    methods: {
        getImagePath: function(img){
            return new URL(`../../../../assets/main-imgs/fitness-section/${img}.jpg`, import.meta.url).href;
        },
    }
}
</script>

<template>
    <div v-for="categoryEl in categoriesList" class="category-card">
        <div class="image-bg">
            <div class="layover"></div>
            <img :src="getImagePath(categoryEl.image)" alt="category image">
        </div>
        <div class="text">
            <DividerComponent id="gray-divider" />
            <h3 class="title">{{ categoryEl.title }}</h3>
            <h5 class="subtitle">{{ categoryEl.subtitle }}</h5>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../../../../styles/partials/variables.scss" as *;
.category-card{
    width: calc((100% / 3) - 2rem);
    position: relative;
    border-radius: 1% 1% 10% 1%;
    overflow: hidden;
    .image-bg{
        width: 100%;
        height: 100%;
        .layover{
            width: 100%;
            height: 100%;
            position: absolute;
            background: linear-gradient(transparent 65%, black);
            // background-color: linear-gradient(to bottom, black, black, black, transparent 60%),
            // rgba(0, 0, 0, 0.7);
        }
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
