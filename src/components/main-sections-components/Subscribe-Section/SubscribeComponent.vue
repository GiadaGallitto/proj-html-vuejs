<script>
import CourseCard from './pseudo-components/CourseCard.vue';
import DividerComponent from '../../DividerComponent.vue';

export default {
    components: {
        CourseCard,
        DividerComponent,
    },
}
</script>

<template>
    
    <section class="fitness-subscribes">
        <article class="upper-sub">
            <div class="sub-infos">
                <h4 class="red-title">Join our mailing list today</h4>
                <h1>Insider offers & flash sales in your inbox every week.</h1>
                <DividerComponent id="yellow-divider" />
                <div class="input-sub">
                    <input placeholder="Insert your e-mail ...*" type="text">
                    <button class="blue-btn" id="sub-btn">Subscribe</button>
                </div>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa sint fuga modi doloremque voluptate et explicabo minus temporibus labore aliquid.</p>
            </div>

            <div class="jumbo-image"></div>
        </article>

        <article class="types-courses wrapper-container">
            <div class="grid-courses">
                <CourseCard />
            </div>
        </article>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../styles/partials/variables.scss" as *;
.fitness-subscribes{
    width: 100%;
    background-color: $CodGrayColor;
    .upper-sub{
        position: relative;
        height: 650px;
        width: 100%;
        display: flex;
        justify-content: end;
        .sub-infos{
            width: 45%;
            position: absolute;
            top: 0;
            left: 15%;
            padding: 6rem 0 7rem;

            h1{
                color: $WhiteColor;
                padding: 0.5rem 0;
                font-size: 3.5rem;
            };

            #yellow-divider{
                color: $YellowColor;
                font-size: 1.2rem;
                margin-bottom: 1.5rem
            };
            .input-sub{
                margin-bottom: 0.8rem;
                input{
                    width: 63%;
                    padding: 0.6rem 1rem;
                    font-size: 1.1rem;
                    border: none;
                    border-radius: 25px;
                    margin-right: 2rem;
                };
                .blue-btn{
                    &#sub-btn{
                        padding-top: 0.8rem;
                        font-size: 1.1rem;
                        width: 32%;
                    };
                };
            };

            p{
                color: $JumboColor;
                padding: 1rem 0;
                font-weight: 500;
                font-size: 1.1rem;
            };
        };
        .jumbo-image{
            height: 100%;
            width: 100%;
            background-image: linear-gradient(to right, #060606, #060606, #060606, transparent 75%),
            url("../../../assets/main-imgs/sub-courses-section/banner1-2x.jpg");
            background-size: 100%;
            background-repeat: no-repeat;
            background-position: top;
        };
    };
    .types-courses{
        height: 770px;
        .grid-courses{
            width: 100%;
            display: flex;
            justify-content: space-between;
            padding-top: 6rem;
        };
    };
};
</style>
