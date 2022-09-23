<template>
    <div class="navbar">
        <router-link to="/" class="link important">
            <img src="/logo.png" alt="Blender Bots Logo" class="logo" />
            Blender Bots
        </router-link>
        <router-link to="/club" class="link">Club</router-link>
        <router-link to="/competitions" class="link">Competitions</router-link>
        <router-link to="/discord" class="link">Discord</router-link>
    </div>
</template>

<style lang="scss" scoped>
$transition: 250ms ease-in-out;

.navbar {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    margin: .25rem .5rem;
    padding: 0;
    height: 4rem;
    background-color: white;

    .link {
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0 1rem;
        padding: 0;
        font-size: 1.3rem;
        font-weight: bold;
        text-decoration: none;
        color: #262424;
        transform: scale(1);
        transition: transform $transition, color $transition;

        &:hover {
            transform: scale(1.05);
            color: #ffb703;
        }

        &.important {
            font-size: 1.6rem;
            margin: 0 2rem;
        }

        .logo {
            width: 3rem;
            height: 3rem;
            margin: 0;
            padding: 0;
        }
    }
}
</style>

<script lang="ts" setup>

</script>
