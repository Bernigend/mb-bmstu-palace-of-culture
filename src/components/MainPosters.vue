<template>
    <section>
        <h2>Афиша</h2>

        <div class="wrapper">
            <div class="posters">
                <div class="poster"></div>
                <div class="poster"></div>
                <div class="poster"></div>
            </div>

            <div class="cntr">
                <Button
                    :text="'Смотреть все'"
                />
            </div>
        </div>
    </section>
</template>

<script>
    import Button from "@/components/Button";

    export default {
        name: "MainPosters",
        components: {
            Button
        }
    }
</script>

<style scoped>
    .posters {
        display: flex;
        margin: 1.5rem -.5rem 2.5rem -.5rem;
        flex-wrap: wrap;
        justify-content: space-around;
    }

    .poster {
        margin: .5rem;
        width: 17.5rem;
        height: 25rem;
        background-color: aquamarine;
        border-radius: 20px;
    }

    .wrapper {
        margin-bottom: 3.5rem;
    }

    @media (max-width: 950px) {
        .poster {
            height: 20.8rem;
            width: 14.5rem;
        }
    }

    @media (max-width: 800px) {
        .poster {
            height: 17rem;
            width: 12rem;
        }
    }
</style>