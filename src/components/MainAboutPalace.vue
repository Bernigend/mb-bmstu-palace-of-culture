<template>
    <section>
        <h2>Дворец культуры</h2>

        <div class="wrapper">
            <div class="img-block">
                <div class="img-with-bg">
                    <img src="../assets/images/bg/assembly-hall-main-view.jpg" alt="Зал Дворца культуры">
                </div>
                <p class="w50">Дворец культуры МГТУ имени Н.Э. Баумана - это построенный в 2004 г. современный культурный комплекс, раполагающий гостиной, кафе, просторными холлами, автопарковкой и современным концертным залом на 1200 мест.</p>
            </div>

            <p class="cntr mtb3">Удобный подъезд, хорошая акустика, современное световое, звуковое и мультимедийное оборудование, а также высококвалифицированный персонал делают данную площадку одним из лучший мест культурного отдыха для студентов, сотрудников и гостей университета.</p>

            <div class="hall-and-conference">
                <div class="hall">
                    <img class="icon" src="../assets/images/icons/assembly-hall.svg" alt="Зал Дворца культуры">
                    <h3>Зал Дворца культуры</h3>
                    <p>Просторный и современный зал для проведения культурно-массовых мероприятий</p>
                    <Button
                        :text="'Подробнее'"
                    />
                </div>

                <div class="conference">
                    <img class="icon" src="../assets/images/icons/conference.svg" alt="Конференц-зал">
                    <h3>Конференц-зал</h3>
                    <p>Просторный и современный зал для проведения культурно-массовых мероприятий</p>
                    <Button
                        :text="'Подробнее'"
                        :colorName="'blue'"
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import Button from "@/components/Button";

    export default {
        name: "MainAboutPalace",
        components: {
            Button
        }
    }
</script>

<style scoped lang="scss">
    @import "../assets/scss/variables";

    section {
        padding: .1px 0;
        background-color: $color-2-lighter;
    }

    h3 {
        font-size: 1.75rem;
        font-weight: 600;
        color: #000000;
    }

    p {
        font-size: 1.3rem;
    }

    .hall-and-conference,
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

    .hall,
    .conference {
        width: 50%;
        padding: 2rem 0;
        text-align: center;

        h3 {
            margin-bottom: 0;
        }

        p {
            margin-top: .5rem;
            font-size: 1.1rem;
        }

        button {
            margin-top: 1rem;
        }
    }

    .hall {
        padding-right: 2rem;
    }

    .conference {
        padding-left: 2rem;
        border-left: 1px solid rgba(96, 109, 113, 0.3);
    }

    .icon {
        width: 100px;
    }

    .wrapper {
        margin-bottom: 3rem;
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

        .hall-and-conference {
            flex-wrap: wrap;
            justify-content: center;
        }

        .hall {
            padding: 3rem 0;
            width: 100%;
            max-width: 500px;
            border: 1px solid rgba(96, 109, 113, 0.3);
            border-right: none;
            border-left: none;
        }

        .conference {
            width: 100%;
            max-width: 500px;
            padding: 3rem 0 0 0;
            border: none;
        }
    }
</style>