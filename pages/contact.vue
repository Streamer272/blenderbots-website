<template>
    <div class="contact-div">
        <div>
            <h1 class="contact-title">Contact us through Gmail,</h1>
            <form class="contact-form" @submit="submit">
                <input class="subject" placeholder="Subject" @change="changeSubject">
                <textarea class="body" placeholder="Body" @change="changeBody"></textarea>
                <button type="submit">Send</button>
            </form>
        </div>

        <div>
            <h1 class="contact-title">or via social media</h1>
            <ul class="social-media-list">
                <li class="social-media" @click="openSocialMedia">
                    <img src="/instagram.png" alt="Instagram Logo">
                    <a href="https://www.instagram.com/blenderbots/" target="_blank">Instagram</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "assets/scss/colors";
@import "assets/scss/mixins";

.contact-div {
    @include flex(row, false);
    margin: 1rem 2rem;
    padding: 0;

    .contact-form {
        display: flex;
        flex-direction: column;
        width: 30vw;
        align-items: flex-end;
        justify-content: center;
        margin: 0 0 0 1.5rem;

        input {
            width: 100%;
            margin: 0;
            padding: .25rem .5rem;
            border-radius: 1rem 1rem 0 0;
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
            border-radius: .5rem .5rem 0 .5rem;
        }
    }

    .social-media-list {
        list-style-type: none;
        margin: 0;
        padding: 0;

        .social-media {
            @include flex(row, true);
            width: fit-content;
            margin: 0 0 0 .5rem;
            cursor: pointer;

            img {
                width: 2rem;
            }

            a {
                color: $black;
                text-decoration: none;
                margin: 0 0 0 .5rem;
                padding: 0;
                font-size: 1.25rem;
            }
        }
    }

    div {
        &:not(:first-of-type) {
            margin: 0 0 0 .5rem;
        }
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

const openSocialMedia = (event) => {
    window.open((event.target.tagName.toLowerCase() === "img" ? event.target.parentElement : event.target).querySelector("a").href)
}
</script>
