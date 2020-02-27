<template>
    <section>
        <BigHeader :title="'Конференц-зал'" />

        <div class="wrapper">
            <div class="img-block">
                <div class="img-with-bg">
                    <img src="../assets/images/bg/assembly-hall-main-view.jpg" alt="Зал Дворца культуры">
                </div>
                <p class="w50">Дворец культуры МГТУ имени Н.Э. Баумана - это построенный в 2004 г. современный культурный комплекс, раполагающий гостиной, кафе, просторными холлами, автопарковкой и современным концертным залом на 1200 мест.</p>
            </div>

            <p class="cntr mtb3">Удобный подъезд, хорошая акустика, современное световое, звуковое и мультимедийное оборудование, а также высококвалифицированный персонал делают данную площадку одним из лучший мест культурного отдыха для студентов, сотрудников и гостей университета.</p>
        </div>
    </section>
</template>

<script>
    import BigHeader from "@/components/BigHeader";

    export default {
        name: "MainAboutConferenceHall",
        components: {
            BigHeader
        }
    }
</script>

<style scoped lang="scss">
    @import "../assets/scss/variables";

    p {
        font-size: 1.3rem;
    }

    .wrapper {
        margin-top: 3rem;
        margin-bottom: 3rem;
    }

    .big-title {
        background-image: url('../assets/images/bg/conference-hall-big-title.jpg');
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