<script>
export default{
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
            <img :src="getImagePath(categoryEl.image)" alt="category image">
        </div>
        <!-- <div class="text">
            {{ categoryEl.title }}
        </div> -->
    </div>

</template>

<style lang="scss" scoped>
.category-card{
    width: calc((100% / 3) - 2rem);
    border: 1px solid black;
    .image-bg{
        width: 100%;
        height: 100%;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}
</style>
