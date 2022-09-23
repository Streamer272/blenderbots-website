<template>
    <form class="contact-form" @submit="submit">
        <input class="subject" placeholder="Subject" @change="changeSubject">
        <textarea class="body" placeholder="Body" @change="changeBody"></textarea>
        <button type="submit">Send</button>
    </form>
</template>

<style lang="scss" scoped>
.contact-form {
    display: flex;
    flex-direction: column;
    width: 30vw;
    align-items: flex-end;
    justify-content: center;
    margin: 1rem 2rem;

    input {
        width: 100%;
        margin: 0;
        padding: .25rem .5rem;
        border-radius: 1rem 0 0 0;
        font-size: 1.2rem;
        border: 1px solid black;
        border-bottom: none;
    }

    textarea {
        width: 100%;
        height: 10rem;
        margin: 0;
        padding: .25rem .5rem;
        border-radius: 0 0 1rem 0;
        font-size: 1rem;
        resize: vertical;
    }

    button {
        width: fit-content;
        margin: .5rem;
        padding: .25rem .75rem;
        font-size: 1.1rem;
        border: 1px solid black;
        border-radius: .5rem;
    }
}
</style>

<script lang="ts" setup>
let subject = ""
let body = ""

const changeSubject = (it) => subject = it.target.value
const changeBody = (it) => body = it.target.value

const submit = () => {
    window.open(`mailto:icrcerevo@gmail.com?subject=${subject}&body=${body}`)
}
</script>
