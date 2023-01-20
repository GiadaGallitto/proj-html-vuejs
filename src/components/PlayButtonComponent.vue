<script>
export default {
    
}
</script>

<template>
    <div id="play-button">
        <i class="fa-solid fa-play"></i>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables.scss" as *;
#play-button{
    cursor: pointer;
    position: absolute;
    color: $DodgerBlueColor;
    background-color: $WhiteColor;
    padding: 2rem 2.5rem;
    border-radius: 50%;
    font-size: 1.2rem;
    transition: all 0.2s ease-in-out;
    &:hover{
        color: $BurntSiennaColor;
    };
};
</style>