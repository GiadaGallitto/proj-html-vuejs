<script>
export default {

}
</script>

<template>
    <div class="footer-container">
        <section class="upper-footer wrapper-container">
            <div class="social">
                <img src="../assets/logo.png" alt="">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure libero rerum, error a nobis mollitia voluptate.</p>
                <span class="social-icons">
                    <a href=""><i class="fa-brands fa-facebook"></i></a>
                    <a href=""><i class="fa-brands fa-twitter"></i></a>
                    <a href=""><i class="fa-brands fa-youtube"></i></a>
                    <a href=""><i class="fa-brands fa-instagram"></i></a>
                    <a href=""><i class="fa-brands fa-linkedin-in"></i></a>
                </span>
            </div>
            <div class="recent-posts">
                <h5>Recent posts</h5>
                <ul>
                    <li><a href=""><i class="fa-solid fa-chevron-right"></i> The best protein shake</a></li>
                    <li><a href=""><i class="fa-solid fa-chevron-right"></i> Ultimate cardio workout</a></li>
                    <li><a href=""><i class="fa-solid fa-chevron-right"></i> New juices available now</a></li>
                    <li><a href=""><i class="fa-solid fa-chevron-right"></i> Tips to find training partners</a></li>
                    <li><a href=""><i class="fa-solid fa-chevron-right"></i> 20 best healthy recipes</a></li>
                </ul>
            </div>
            <div class="contacts">
                <h5>Contacts informations</h5>
                <p>4746 Tipple Road Michigan 48449</p>
                <h6>Mobile: 1.800.000.0000</h6>
                <h6>Email: info@your-company.com</h6>
            </div>
        </section>
        <section class="lower-footer">
            <p>Copyright 2012 - 2020 | Avada theme by <span><a href="">ThemeFusion</a></span> | All rights reserved | Powered by <span><a href="">WordPress</a></span></p>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables.scss" as *;
.footer-container {
    width: 100%;
    background-color: black;
    color: $WhiteColor;
    .upper-footer {
        display: flex;
        justify-content: space-between;
        padding: 7rem 0;
        div{
            width: calc(100% / 3);
            text-align: center;
            padding: 3rem 3.5rem;
            display: flex;
            flex-direction: column;
            align-items: center;

            h5{
                text-transform: uppercase;
                margin-bottom: 1.5rem;
                font-size: 1.1rem;
            };
            &.social{
                img{
                    margin-bottom: 2.5rem;
                };

                p{
                    margin-bottom: 2rem;
                };
                .social-icons{
                    i{
                        margin: 0 0.5rem;
                        font-size: 1.1rem;
                        color: $BurntSiennaColor;
                    };
                };
            };
            &.recent-posts{
                ul{
                    list-style-type: none;
                    padding: 0;
                    li{
                        line-height: 3rem;
                        font-size: 1.1rem;
                        a{
                            color: $WhiteColor;
                            transition: all 0.3s ease-in-out;
                            i{
                                font-size: 0.9rem
                            };
                        };
                        &:hover a{
                            color: $DodgerBlueColor;
                        };
                    };
                };
            };
            &.contacts{
                p{
                    line-height: 2.2rem;
                    color: $SilverColor;
                };

                h6{
                    margin: 0.3rem 0 0.1rem;
                };
            };
        };
    };
    .lower-footer {
        border-top: 1px solid $JumboColor;
        padding: 2.5rem 0 2rem;
        font-size: 1.1rem;
        text-align: center;
        color: $JumboColor;
        span a{
            color: $WhiteColor;
            &:hover{
                color: $DodgerBlueColor;
            };
        };
    };
};
</style>
