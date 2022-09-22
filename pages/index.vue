<template>
    <div>
        <button class="count-button" v-on:click="count++">You clicked me <span class="count">{{ count }}</span> times</button>
    </div>
</template>

<style lang="scss" scoped>
.count-button {
    color: #eeeeee;
    background-color: #ff2400;
    border: none;
    border-radius: .5rem;
    font-size: 1.25rem;
    margin: 0;
    padding: .25rem .3rem;
    cursor: pointer;

    .count {
        color: gold;
    }
}
</style>

<script lang="ts" setup>
const count = ref(0);
</script>
