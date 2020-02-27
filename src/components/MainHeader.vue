<template>
    <header>
        <!--  Контакты  -->
        <div class="contacts">
            Контакты
        </div>

        <!--  Заголовок  -->
        <h1 class="title">
            <span class="first"><span>Дворец</span> <span>культуры</span></span>
            <span class="second"><span>МФ МГТУ им.</span> <span>Н.Э. Баумана</span></span>
        </h1>

        <!--  Кнопки  -->
        <div class="buttons">
            <div class="group">
                <Button
                    :text="'Афиша'"
                />
                <Button
                    :text="'О дворце'"
                />
            </div>
            <div class="group">
                <Button
                    :text="'Студия'"
                    :colorName="'blue'"
                />
                <Button
                    :text="'Аренда'"
                    :colorName="'blue'"
                />
            </div>
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
        display: flex;
        justify-content: center;
        align-items: center;

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
        position: absolute;
        top: 2rem;
        right: 2rem;
        font-size: 1.125rem;
        z-index: 2;
    }

    .title {
        font-size: 1rem;
        /*<!--position: absolute;-->*/
        /*<!--top: 50%;-->*/
        /*<!--margin-top: -80px;-->*/
        /*<!--left: 50%;-->*/
        /*<!--margin-left: -335.5px;-->*/

        /*display: inline-block;*/
        padding: 0 2rem 1rem 2rem;

        border: 3px solid #ffffff;
        border-top: none;
        border-bottom: none;

        font-weight: bold;
        z-index: 2;

        .first {
            display: block;
            font-size: 4.625em;
        }

        .second {
            font-size: 3em;
        }
    }

    .buttons {
        display: flex;
        position: absolute;
        //margin: -.5rem;
        padding: 0 2rem;

        width: 100%;
        max-width: 800px;

        bottom: 2rem;

        flex-wrap: wrap;
        justify-content: space-around;

        z-index: 2;
        //left: 50%;
        //margin-left: -348px;

        .group {
            display: flex;
            width: 100%;
            max-width: 23rem;
            justify-content: space-around;
        }
    }

    button {
        width: 150px;
        margin: .5rem;

        //margin-right: 2rem;

        /*&:last-child {*/
        /*    margin-right: 0;*/
        /*}*/
    }

    @media (max-width: 780px) {
        .title {
            font-size: .8rem;
        }
    }

    @media (max-width: 650px) {
        .title {
            font-size: .6rem;
        }
    }

    @media (max-width: 540px) {
        .title {
            font-size: .5rem;

            .first {
                span:first-child {
                    display: block;
                    font-size: 1.23em;
                }
            }

            .second {
                span:first-child {
                    display: block;
                    padding-top: 1rem;
                    font-size: 1.07em;
                }

                span:last-child {
                    font-size: 1.1em;
                }
            }
        }
    }
</style>