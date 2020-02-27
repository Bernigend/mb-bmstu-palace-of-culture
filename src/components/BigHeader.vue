<template>
    <section class="big-title">
        <h2>{{ title }}</h2>
    </section>
</template>

<script>
    export default {
        name: "BigHeader",
        props: ['title']
    }
</script>

<style scoped lang="scss">
    section {
        position: relative;
        padding: 5rem 0;

        font-size: 1rem;
        text-align: center;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;

        &::after {
            display: block;
            content: '';

            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;

            background-color: rgba(0,0,0,0.7);
            z-index: 1;
        }
    }

    h2 {
        display: inline-block;
        position: relative;
        margin: 0;
        padding: 0 3rem .7rem 3rem;

        border: 3px solid #ffffff;
        border-top: none;
        border-bottom: none;

        font-family: 'Exo 2',serif;
        font-size: 2.3em;

        color: #ffffff;
        z-index: 5;
    }

    @media (max-width: 560px) {
        section {
            font-size: .7rem;
        }

        h2 {
            padding-right: 1.5rem;
            padding-left: 1.5rem;
        }
    }
</style>