<template>
    <section>
        <!--  Заголовок  -->
        <BigHeader
            :title="'Зал Дворца культуры'"
        />

        <div class="wrapper">

            <!--  Общие цифры  -->
            <div class="numbers">
                <div class="number">
                    1200<br>мест
                </div>
                <div class="number blue">
                    <div>1500<br>м<sup>2</sup></div>
                </div>
                <div class="number">
                    1200<br>мест
                </div>
            </div>

            <!--  Навигация  -->
            <div class="navigation">
                <Button :text="'Сцена'" />
                <Button :text="'Звук'" :colorName="'blue'" :no-bg="true" />
                <Button :text="'Свет'" :no-bg="true" />
                <Button :text="'Кино'" :colorName="'blue'" :no-bg="true" />
                <Button :text="'Тех. райдер'" :no-bg="true" />
            </div>

            <!--  Информация из навигации  -->
            <div class="info">
                <div class="img-block">
                    <div class="img-with-bg">
                        <img src="../assets/images/bg/assembly-hall-main-view.jpg" alt="Зал Дворца культуры">
                    </div>
                    <p class="w50">Дворец культуры МГТУ имени Н.Э. Баумана - это построенный в 2004 г. современный культурный комплекс, раполагающий гостиной, кафе, просторными холлами, автопарковкой и современным концертным залом на 1200 мест.</p>
                </div>

                <p class="cntr mtb3">Удобный подъезд, хорошая акустика, современное световое, звуковое и мультимедийное оборудование, а также высококвалифицированный персонал делают данную площадку одним из лучший мест культурного отдыха для студентов, сотрудников и гостей университета.</p>
            </div>

        </div>
    </section>
</template>

<script>
    import BigHeader from "@/components/BigHeader";
    import Button from "@/components/Button";

    export default {
        name: "MainAboutAssemblyHall",
        components: {
            BigHeader,
            Button
        }
    }
</script>

<style scoped lang="scss">
    @import "../assets/scss/variables";

    p {
        font-size: 1.3rem;
    }

    button {
        &.no-bg {
            font-weight: 600;
        }
    }

    .big-title {
        background-image: url('../assets/images/bg/assembly-hall-big-title.jpg');
    }

    .numbers,
    .navigation {
        display: flex;
        margin: 3.5rem -.5rem;

        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;
    }

    .numbers {
        .number {
            display: flex;
            width: 160px;
            height: 160px;
            margin: .5rem;

            align-items: center;
            justify-content: center;

            font-size: 2rem;
            font-weight: 600;
            text-align: center;

            border: 15px solid $color-1;
            border-radius: 200px;

            sup {
                font-size: .9rem;
            }

            &.blue {
                border-color: $color-2;
            }
        }
    }

    .navigation {
        button {
            margin: .5rem;
        }
    }

    .img-block {
        display: flex;
        flex-wrap: nowrap;
        align-items: center;
        justify-content: space-between;
    }

    .img-with-bg {
        width: 45%;
        transform: rotate(-3deg);
        position: relative;

        img {
            position: relative;
            width: 100%;
            z-index: 5;
        }

        &:after {
            display: block;
            content: '';

            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;

            background-color: $color-2-light;
            transform: rotate(3deg);
            z-index: 1;
        }
    }

    @media (max-width: 750px) {
        .img-block {
            flex-wrap: wrap;
            justify-content: center;
        }

        .img-with-bg {
            width: 70%;
        }

        .img-block {
            p {
                width: auto;
                text-align: center;
                margin: 3rem 0 0 0;
            }
        }
    }
</style>