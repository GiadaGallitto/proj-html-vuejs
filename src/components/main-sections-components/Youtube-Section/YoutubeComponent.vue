<script>
import YoutubeCard from './pseudo-components/YoutubeCard.vue';
import PlayButtonComponent from '../../PlayButtonComponent.vue';

export default {
    components: {
        YoutubeCard,
        PlayButtonComponent,
    }
}
</script>

<template>
    <section class="youtube-features">
        <article class="main-youtube flex-container">
            <div class="main-video">
                <!-- Immagine e Component Play Button -->
                <PlayButtonComponent class="youtube-play" />
            </div>
            <div class="youtube-infos">
                <!-- Testo con info canale youtube e button -->
                <h3>Tune up your workouts</h3>
                <h1>The best health & fitness advice online</h1>
                <div class="yt-channel">
                    <img src="../../../assets/unnamed.jpg" alt="icon-yt" class="icon">
                    <div class="channel-info">
                        <p class="name-channel">ThemeFusion</p>
                        <div class="channel-sub">
                            <span id="red-part"><i class="fa-brands fa-youtube pe-2 fs-6"></i>Youtube</span>
                            <span id="white-part">999+</span>
                        </div>
                    </div>
                </div>
                <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Itaque, sequi dolorem exercitationem provident cum obcaecati fugit.</p>
                <button class="blue-btn" id="red-btn">
                    <i class="fa-brands fa-youtube pe-2 fs-6"></i>
                    Visit my Youtube channel
                </button>
            </div>
        </article>

        <article class="features-youtube wrapper-container">
            <!-- Micro component con all'interno alcuni dei video da inserire con js -->
            <div class="tools">
                <h3>Featured playlists</h3>
                <h5>
                    View all videos
                    <i class="fa-solid fa-chevron-right"></i>
                </h5>
            </div>
            <div class="grid-videos">
                <YoutubeCard />
            </div>
        </article>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
.youtube-features{
    height: 600px;
    position: relative;
    .main-youtube{
        position: relative;
        display: flex;
        justify-content: flex-end;
        height: 750px;
        .main-video{
            width: 50%;
            height: 100%;
            background-image: url("../../../assets/main-imgs/youtube-section/service15-2x.jpg");
            background-size: cover;
            border-radius: 0% 1% 5% 0%;
            overflow: hidden;
            position: absolute;
            left: 0;
            top: -7%;
            .youtube-play{
                top: 50%;
                left: 50%;
                transform: translate(-50% , -50%);
            }
        };
        .youtube-infos{
            width: 50%;
            padding: 8rem;
            h3{
                color: $DodgerBlueColor;
            };

            h1{
                font-size: 3rem;
                margin: 2rem 0;
            };
            .yt-channel{
                display: flex;
                margin-bottom: 1.5rem;
                img{
                    width: 50px;
                    height: 50px;
                    margin-right: 1rem;
                };
                .name-channel{
                    font-size: 1rem;
                    color: $JumboColor;
                    font-weight: 500;
                    display: inline;
                };
                .channel-sub{
                    font-weight: 500;
                    margin-top: 0.5rem;

                    #red-part{
                        color: white;
                        background-color: red;
                        border: 1px solid $MonzaColor;
                        padding: 0.2rem 0.5rem 0.3rem;
                    };

                    #white-part{
                        color: $JumboColor;
                        padding: 0.2rem 0.5rem 0.3rem;
                        border: 1px solid $JumboColor;
                    }
                }
            };
            .blue-btn{
                &#red-btn{
                    margin-top: 1rem;
                    background-color: red;
                    border: none;
                    font-size: 1.1rem;
                    padding-top: 0.7rem;
                }
            }
        }
    };
    .features-youtube{
        .tools{
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 2rem;

            i{
                font-size: 1rem;
                padding-left: 0.2rem;
            }
        }
        .grid-videos{
            display: flex;
            justify-content: space-between;
            width: 100%;
        }
    }
}
</style>
