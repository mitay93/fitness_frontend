<template>
    <div class="main-content">
        <MainIntroduction />

        <MainSlider />
    </div>
</template>

<script>
import MainIntroduction from "@/components/shared/main/introduction/introduction.vue";
import MainSlider from "@/components/shared/main/slider/slider.vue";

export default {
    name: "MainContent",
    components: {
        MainIntroduction,
        MainSlider,
    },
};
</script>

<style lang="scss">
.main-content {
    display: flex;
    min-height: 100vh;
}

@media screen and (max-width: 1024px) {
    .main-content {
        flex-direction: column-reverse;
    }
}
</style>
