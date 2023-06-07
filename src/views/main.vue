<template>
    <div class="main">
        <MainContent />
    </div>
</template>

<script>
import MainContent from "@/components/shared/main/content/content.vue";

export default {
    name: "Main",
    components: {
        MainContent,
    },
};
</script>

<style lang="scss">
.main {
    min-height: 100vh;
}
</style>
