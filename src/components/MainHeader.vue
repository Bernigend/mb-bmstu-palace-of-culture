<template>
    <header>
        <!--  Контакты  -->
        <div class="contacts">
            Контакты
        </div>

        <!--  Заголовок  -->
        <h1 class="title">
            <span class="first">Дворец культуры</span>
            <span class="second">МФ МГТУ им. Н.Э. Баумана</span>
        </h1>

        <!--  Кнопки  -->
        <div class="buttons">
            <Button
                :text="'Афиша'"
            />
            <Button
                :text="'О дворце'"
            />
            <Button
                :text="'Студия'"
                :colorName="'blue'"
            />
            <Button
                :text="'Аренда'"
                :colorName="'blue'"
            />
        </div>
    </header>
</template>

<script>
    import Button from "@/components/Button";

    export default {
        name: "MainHeader",
        components: {
            Button
        }
    }
</script>

<style scoped lang="scss">
    header {
        position: relative;
        width: 100%;
        height: 100vh;

        padding: 2rem;

        color: rgb(255, 255, 255);

        background-image: url('../assets/images/bg/assembly-hall-main-view.jpg');
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

    .contacts {
        position: relative;
        float: right;
        font-size: 1.125rem;
        z-index: 2;
    }

    .title {
        position: absolute;
        top: 50%;
        margin-top: -80px;
        left: 50%;
        margin-left: -335.5px;

        display: inline-block;
        padding: 0 2rem 1rem 2rem;

        border: 3px solid #ffffff;
        border-top: none;
        border-bottom: none;

        font-weight: bold;
        z-index: 2;

        .first {
            display: block;
            font-size: 4.625rem;
        }

        .second {
            font-size: 3rem;
        }
    }

    .buttons {
        position: absolute;
        bottom: 2rem;
        z-index: 2;
        left: 50%;
        margin-left: -348px;
    }

    button {
        width: 150px;
        margin-right: 2rem;

        &:last-child {
            margin-right: 0;
        }
    }
</style>