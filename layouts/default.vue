<template>
    <Navbar />
    <slot />
</template>

<style lang="scss">
body {
    margin: 0;
    padding: 0;
    background-color: #ffffff;
}

.page {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
}
</style>

<script lang="ts" setup>

</script>
