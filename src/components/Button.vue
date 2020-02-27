<template>
    <button :class="{ 'blue': colorName === 'blue', 'no-bg': noBg === true }">
        {{ text }}
    </button>
</template>

<script>
    export default {
        name: "Button",
        props: ['text', 'colorName', 'noBg']
    }
</script>

<style scoped lang="scss">
    @import "../assets/scss/variables";

    button {
        padding: .9rem 2.5rem;
        border: 2px solid $color-1;
        border-radius: 50px;

        font-family: 'Exo 2',serif;
        font-size: 0.875rem;
        color: #fff;
        background-color: $color-1;
        text-transform: uppercase;

        cursor: pointer;
        transition: .2s background-color ease-in,
                    .2s border ease-in;

        &.blue {
            background-color: $color-2;
            border-color: $color-2;

            &:hover,
            &:not(.no-bg):hover {
                border-color: $color-2-hover;
            }

            &:not(.no-bg):hover {
                background-color: $color-2-hover;
            }
        }

        &.no-bg {
            background: none;
            color: #000000;
            border-color: transparent;
        }

        &:hover {
            border-color: $color-1-hover;
        }

        &:not(.no-bg):hover {
            background-color: $color-1-hover;
            border-color: $color-1-hover;
        }

        &:focus {
            outline: none;
        }
    }
</style>