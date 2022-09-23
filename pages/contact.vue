<template>
    <form class="contact-form" @submit="submit">
        <input id="subject" placeholder="Subject" @change="changeSubject">
        <input id="body" placeholder="Message" @change="changeMessage">
        <button type="submit">Send</button>
    </form>
</template>

<style lang="scss" scoped>
.contact-form {

}
</style>

<script lang="ts" setup>
let subject = ""
let message = ""

const changeSubject = (it) => subject = it.target.value
const changeMessage = (it) => message = it.target.value

const submit = () => {
    window.open(`mailto:icrcerevo@gmail.com?subject=${subject}&body=${message}`)
}
</script>
