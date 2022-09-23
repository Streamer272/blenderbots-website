<template>
    <div class="page">
        <h1 class="title">404</h1>
        <h3 class="subtitle">Page not found</h3>
        <button @click="redirect" class="redirect">Go back home</button>
    </div>
</template>

<style lang="scss" scoped>
.page {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;

    .title {
        font-size: 5rem;
        margin: .25rem;
        padding: 0;
    }

    .subtitle {
        font-size: 2.30rem;
        margin: .25rem;
        padding: 0;
    }

    .redirect {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-size: 1.05rem;
        background: transparent;
        border: none;
        width: fit-content;
        height: fit-content;
        margin: 1.25rem;
        padding: .5rem 1rem;
        cursor: pointer;

        &:after {
            content: "";
            margin: .25rem 0 0 0;
            padding: 0;
            display: block;
            width: 85%;
            height: 2px;
            background: black;
            transition: width 250ms ease-in-out;
        }

        &:hover {
            &:after {
                width: 95%;
            }
        }
    }
}
</style>

<script lang="ts" setup>
const router = useRouter()

const redirect = () => {
    router.push('/')
}
</script>
