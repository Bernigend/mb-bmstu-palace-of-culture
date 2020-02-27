<template>
    <section>
        <h2>Аренда</h2>

        <div class="wrapper">
            <!--  Навигация  -->
            <div class="navigation">
                <Button :text="'Зал ДК'" :colorName="'blue'" />
                <Button :text="'Холл ДК'" :no-bg="true" />
                <Button :text="'Конференц-зал'" :colorName="'blue'" :no-bg="true" />
                <Button :text="'Костюмы'" :no-bg="true" />
                <Button :text="'Студии'" :colorName="'blue'" :no-bg="true" />
            </div>

            <div class="cntr">Что-нибудь об аренде</div>
        </div>
    </section>
</template>

<script>
    import Button from "@/components/Button";

    export default {
        name: "MainRent",
        components: {
            Button
        }
    }
</script>

<style scoped lang="scss">
    .wrapper {
        margin-bottom: 3rem;
    }

    .navigation {
        display: flex;
        margin: 2.5rem -.5rem;

        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;

        button {
            margin: .5rem;
        }
    }
</style>