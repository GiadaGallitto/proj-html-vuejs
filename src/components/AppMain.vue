<script>
// Qui verranno importati i macro componenti delle sezioni, ciascuna sezione conterrà a sua volta micro componenti per le schede ripetute
export default{

}
</script>

<template>
    <div class="main-container">
        <div class="wrapper-container">
            <section class="fitness-categories">
                <!-- Micro component con all'interno le categorie di fitness mostrate con js -->
                <div class="quote">
                    <!-- Contenitore di testo con citazione, divider e nome/luogo della persona (per la struttura di questo -> classe e modifica unica per tutte le simili) -->
                </div>
            </section>

            <section class="youtube-features">
                <article class="main-youtube flex-container">
                    <div class="main-video">
                        <!-- Immagine e Component Play Button -->
                    </div>
                    <div class="youtube-infos">
                        <!-- Testo con info canale youtube e button -->
                    </div>
                </article>
                <article class="features-youtube">
                    <!-- Micro component con all'interno alcuni dei video da inserire con js -->
                </article>
            </section>

            <section class="fitness-subscribes">
                <article class="upper-sub">
                    <!-- Mini jumbo con background-image -->
                    <div class="sub-infos">
                        <!-- Contenitore di testo a sinistra con info per il subscribe -->
                    </div>
                </article>
                <article class="types-courses">
                    <!-- Micro component con all'interno alcuni dei corsi da inserire con js -->
                </article>
            </section>

            <section class="articles-sales">
                <article class="latest-articles">
                    <!-- Micro component con all'interno alcuni degli ultimi articoli da inserire con js -->
                </article>
                <article class="main-sales">
                    <!-- Mini jumbo con background-image -->
                    <div class="quote-sales">
                        <!-- Contenitore di testo al centro con una quote e un button per acquistare -->
                    </div>
                </article>
            </section>

            <section class="partners">
                <article class="partners-cards">
                    <!-- Micro component con all'interno i partners da inserire con js -->
                </article>
            </section>

            <section class="daily-workout">
                <!-- Mini jumbo con background-image -->
                <article class="work-day">
                    <!-- Contenitore di testo al centro con le info del workout giornaliero-->
                </article>
            </section>
        </div>
    </div>
</template>

<style lang="scss">

</style>
