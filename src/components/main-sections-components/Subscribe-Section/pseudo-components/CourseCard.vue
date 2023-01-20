<script>
export default{
    components: {
    },

    data(){
        return {
            courseList: [
                {
                    image: 'watch',
                    title: "Team training",
                    subtitle: "Find a partner",
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi, velit. Quidem nulla veritatis dignissimos nostrum saepe. Cupiditate, voluptates quasi.",
                    info: "Find a partner"
                },
                {
                    image: 'dumbbell',
                    title: "Crossfit workout",
                    subtitle: "Push your limits",
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi, velit. Quidem nulla veritatis dignissimos nostrum saepe. Cupiditate, voluptates quasi.",
                    info: "Learn about Crossfit"
                },
                {
                    image: 'slim',
                    title: "Weight loss plan",
                    subtitle: "Shed those pounds",
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi, velit. Quidem nulla veritatis dignissimos nostrum saepe. Cupiditate, voluptates quasi.",
                    info: "Schedule a workout"
                },
            ]
        }
    },

    methods: {
        getImagePath: function(img){
            return new URL(`../../../../assets/main-imgs/sub-courses-section/${img}.png`, import.meta.url).href;
        },
    }
}
</script>

<template>
    <div v-for="courseEl in courseList" class="course-card">
        <div class="image-icon">
            <img :src="getImagePath(courseEl.image)" alt="course image">
        </div>
        <div class="text">
            <h3 class="title">{{ courseEl.title }}</h3>
            <h5 class="subtitle">{{ courseEl.subtitle }}</h5>
            <p class="text">{{ courseEl.text }}</p>
            <h6 class="info">{{ courseEl.info }}<i class="fa-solid fa-chevron-right"></i></h6>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../../../../styles/partials/variables.scss" as *;
.course-card{
    width: calc((100% / 3) - 2rem);
    position: relative;
    border: 4px solid $DodgerBlueColor;
    border-radius: 5px;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 5rem 3.2rem;
    .image-icon{
        img{
            width: 70px;
            height: 70px;
            margin-bottom: 2rem;
        }
    }
    .text{
        text-align: center;
        .title{
            color: $WhiteColor;
            font-size: 2rem;
            line-height: 1.7rem;
            margin-bottom: 1rem;
        };
        .subtitle{
            color: $YellowColor;
            font-size: 1.6rem;
            margin-bottom: 2.2rem;
        };
        .text{
            color: $SilverColor;
            font-weight: 500;
            margin-bottom: 2.2rem
        };
        .info{
            color: $WhiteColor;
            .fa-chevron-right{
                font-size: 0.7rem;
                margin-left: 0.4rem;
            }
        }
    }
}
</style>
