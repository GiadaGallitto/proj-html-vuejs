<script>
import DividerComponent from '../../../DividerComponent.vue';

export default{
    components: {
        DividerComponent,
    },

    data(){
        return {
            partnerList: [
                {
                    image: 'sponsor-1-2x',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi, velit. Quidem nulla veritatis dignissimos.",
                    info: "Visit Yoga Studio"
                },
                {
                    image: 'sponsor-2-2x',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi, velit. Quidem nulla veritatis dignissimos.",
                    info: "Join Fitness Center"
                },
                {
                    image: 'sponsor-3-2x',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi, velit. Quidem nulla veritatis dignissimos.",
                    info: "Learn about FC"
                },
                {
                    image: 'sponsor-4-2x',
                    text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi, velit. Quidem nulla veritatis dignissimos.",
                    info: "Visit Power Gym"
                },
            ]
        }
    },

    methods: {
        getImagePath: function(img){
            return new URL(`../../../../assets/main-imgs/partners-section/${img}.png`, import.meta.url).href;
        },
    }
}
</script>

<template>
    <div v-for="partnerEl in partnerList" class="partner-card">
        <div class="image-icon">
            <img :src="getImagePath(partnerEl.image)" alt="partner image">
        </div>
        <DividerComponent id="blue-divider" />
        <div class="text-card">
            <p class="text">{{ partnerEl.text }}</p>
            <h6 class="info">{{ partnerEl.info }}<i class="fa-solid fa-chevron-right"></i></h6>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../../../../styles/partials/variables.scss" as *;
.partner-card{
    cursor: pointer;
    width: calc((100% / 4) - 2rem);
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2.5rem 1.3rem;
    .image-icon{
        padding: 0 1.8rem;
        img{
            margin-bottom: 0.5rem;
            width: 100%;
        }
    };

    #blue-divider{
        color: $DodgerBlueColor;
        font-size: 1.3rem;
        margin-bottom: 1.2rem;
    }
    .text-card{
        text-align: center;
        .text{
            color: $JumboColor;
            font-weight: 500;
            margin-bottom: 2.2rem
        };
        .info{
            font-weight: 600;
            .fa-chevron-right{
                font-size: 0.8rem;
                margin-left: 0.3rem;
            }
        }
    }
}
</style>
