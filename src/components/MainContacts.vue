<template>
    <section>
        <BigHeader :title="'Контакты'" />

        <div class="wrapper">
<!--            <img class="logo" src="../assets/images/bmstu-logo.png" alt="Логотип МГТУ им. Н.Э. Баумана">-->
            <address>
                <div class="contacts">
                    <div><a href="tel:+71233457854">8 (497) 542-67-98</a></div>
                    <div><a href="mailto:palace-of-culture@yandex.ru">palace-of-culture@yandex.ru</a></div>
                    <div><a href="tel:+71233457854">8 (497) 543-56-43</a></div>
                </div>
                <div class="address"><strong>Адрес:</strong> 141005, Московская обл., г. Мытищи, 1-я Институтская, д. 1, Мытищинский филиал МГТУ им. Н.Э. Баумана</div>
            </address>

            <div class="buttons">
                <Button :text="'Открыть Яндекс.Карты'" />
                <Button :text="'Открыть Google Maps'" :colorName="'blue'" />
            </div>

<!--            <div class="map-big">-->
<!--                <script type="application/javascript" charset="utf-8" async src="https://api-maps.yandex.ru/services/constructor/1.0/js/?um=constructor%3A767ab5fe6e40718a0d063d1778367d02194dc66279bac6f59f4a900b3c9975f8&amp;width=100%25&amp;height=316&amp;lang=ru_RU&amp;scroll=true"></script>-->
<!--            </div>-->

<!--            <div class="map-small">-->
<!--                <a href="https://yandex.ru/maps/?um=constructor%3A767ab5fe6e40718a0d063d1778367d02194dc66279bac6f59f4a900b3c9975f8&amp;source=constructorStatic" target="_blank"><img src="https://api-maps.yandex.ru/services/constructor/1.0/static/?um=constructor%3A767ab5fe6e40718a0d063d1778367d02194dc66279bac6f59f4a900b3c9975f8&amp;width=600&amp;height=450&amp;lang=ru_RU" alt="" style="border: 0;" /></a>-->
<!--            </div>-->
        </div>
    </section>
</template>

<script>
    import BigHeader from "@/components/BigHeader";
    import Button from "@/components/Button";

    export default {
        name: "MainContacts",
        components: {
            BigHeader,
            Button
        }
    }
</script>

<style scoped lang="scss">
    @import "../assets/scss/variables";

    section {
        //background-color: $color-2-lighter;
    }

    address {
        font-style: normal;
        font-size: 1.1rem;
    }

    button {
        margin: .5rem;
    }

    .buttons {
        margin: -.5rem;
        text-align: center;
    }

    .contacts {
        display: flex;
        margin: 0 -.5rem;
        justify-content: space-around;
        font-weight: 600;
        flex-wrap: wrap;

        div {
            margin: .5rem;
            padding: 1rem 2rem;
            border: 2px solid $color-2;
            border-radius: 100px;

            &:nth-child(2) {
                border-color: $color-1;
            }
        }

        a {
            color: inherit;
            text-decoration: none;

            &:hover {
                text-decoration: underline;
            }
        }
    }

    .address {
        /*font-size: 1.3rem;*/
        text-align: center;
        margin: 2.5rem 0 3rem 0;
    }

    .wrapper {
        padding-top: 2.5rem;
        padding-bottom: 3rem;

        &:after {
            display: block;
            content: '';
            clear: both;

        }
    }

    .big-title {
        background-image: url('../assets/images/bg/mb-bmstu.jpg');
    }

    .logo {
        height: 200px;
        float: left;
    }
</style>