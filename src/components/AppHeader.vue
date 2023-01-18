<script>
    export default{

    }
</script>

<template>
    <div class="header-container">
        <!-- Qui inserirò il la barra nera che conterrà logo e nav-bar -->
        <div class="upper-bar">
            <div class="logo"></div>
            <div class="nav-bar"></div>
        </div>
        <!-- Qui inserirò il jumbotron con background-image e il container di testo a sinisra del jumbo (va aggiunto anche il componentPlayButton) -->
        <div class="jumbotron">
            <div class="jumbo-text"></div>
            <!-- Component Play Button -->
            <div class="jumbo-details">
                <!-- Elementi di dettaglio a destra del jumbotron -->
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.header-container{
    width: 100%;
}
</style>
