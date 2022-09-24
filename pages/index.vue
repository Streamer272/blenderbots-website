<template>
    <div>
        <section class="title-section" style="background-image: url(/logo.png);">
            <h1 class="title">Blender Bots</h1>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@import "../assets/scss/colors";

section {
    background-repeat: no-repeat;
    background-position: right;
    background-size: contain;
    height: 100vh;

    &.title-section {
        display: flex;
        align-items: center;
        justify-content: flex-start;

        .title {
            font-size: 3.5rem;
            margin-left: 10%;
        }
    }

    &:first-of-type {
        height: calc(100vh - 4rem);
    }
}
</style>

<script lang="ts" setup>

</script>
