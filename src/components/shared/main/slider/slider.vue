<template>
    <div class="main-slider">
        <swiper
            class="main-slider__swiper"
            :centeredSlides="true"
            :autoplay="{
                delay: 3000,
                disableOnInteraction: false,
            }"
            :pagination="{
                clickable: true,
            }"
            :modules="modules"
        >
            <swiper-slide
                class="main-slider__slide"
                v-for="slide in getSlides"
                :key="slide.id"
            >
                <img
                    class="main-slider__slide-image"
                    :src="slide.img"
                    alt="slide"
                />
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
import {Swiper, SwiperSlide} from "swiper/vue";
import {Autoplay, Pagination} from "swiper";

import "swiper/css";
import "swiper/css/pagination";

export default {
    name: "MainSlider",
    components: {
        Swiper,
        SwiperSlide,
    },
    data() {
        return {
            modules: [Autoplay, Pagination],
        };
    },
    computed: {
        getSlides() {
            return [
                {
                    id: 0,
                    img: require("@/assets/images/shared/main/slider/slide-1.png"),
                },
                {
                    id: 1,
                    img: require("@/assets/images/shared/main/slider/slide-2.png"),
                },
                {
                    id: 2,
                    img: require("@/assets/images/shared/main/slider/slide-3.png"),
                },
                {
                    id: 3,
                    img: require("@/assets/images/shared/main/slider/slide-4.png"),
                },
                {
                    id: 4,
                    img: require("@/assets/images/shared/main/slider/slide-5.png"),
                },
            ];
        },
    },
};
</script>

<style lang="scss">
.main-slider {
    width: 100%;
    max-width: 805px;

    .main-slider__swiper {
        height: 100%;
    }

    .main-slider__slide-image {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .swiper-pagination {
        bottom: 80px;
    }

    .swiper-pagination-bullet {
        width: 20px;
        height: 20px;
        background: rgba(255, 255, 255, 0.5);
        opacity: 1;
    }

    .swiper-pagination-bullet-active {
        background: $white;
        opacity: 1;
    }
}

@media screen and (max-width: 1024px) {
    .main-slider {
        max-width: 100%;

        .swiper-pagination {
            bottom: 16px;
        }

        .swiper-pagination-bullet {
            width: 12px;
            height: 12px;
        }
    }
}
</style>
