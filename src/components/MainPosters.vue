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
        margin: 2rem 0;
        flex-wrap: nowrap;
        justify-content: space-between;
    }

    .poster {
        width: 17.5rem;
        height: 25rem;
        background-color: aquamarine;
        border-radius: 20px;
    }

    .wrapper {
        margin-bottom: 3.5rem;
    }
</style>