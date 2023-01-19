<script>
export default {

}
</script>

<template>
    <div class="header-container">
        <!-- Qui inserirò il la barra nera che conterrà logo e nav-bar -->
        <div class="upper-bar wrapper-container">
            <div class="logo w-25">
                <img src="../assets/logo.png" alt="">
            </div>
            <ul class="nav-bar">
                <li>Home</li>
                <li>Services</li>
                <li>About</li>
                <li>Videos</li>
                <li>Blog</li>
                <li>
                    Store
                    <span id="new-btn">new</span>
                </li>
                <li>
                    <button class="blue-btn">Schedule a workout</button>
                </li>
            </ul>
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
@use "../styles/partials/variables.scss" as *;

.header-container {
    background-color: $CodGrayColor;

    .upper-bar {
        height: 100%;
        padding: 1.8rem 0;
        justify-content: space-between;
        display: flex;
        align-items: center;

        .nav-bar {
            list-style-type: none;
            margin-bottom: 0;

            li {
                display: inline-block;
                color: $SilverColor;
                padding: 0 1.2rem;
                #new-btn{
                    font-size: 0.9rem;
                    margin-left: 0.6rem;
                    padding: 0.4rem 0.6rem;
                    color: black;
                    background-color: #fff941;
                    border-radius: 2px;
                }
            }
        }
    }
}


// Ogni wrapper container all'interno dei components principali avrà una width fissa
</style>
