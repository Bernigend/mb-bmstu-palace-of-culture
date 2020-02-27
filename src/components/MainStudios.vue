<template>
    <section>
        <div class="studio">
            <div class="img sound"></div>
            <div class="text">
                <div class="info">
                    <h3>Студия звукозаписи</h3>
                    <p>Записывайте свои треки на современном оборудовании в хорошем качестве</p>
                    <Button
                        :text="'Подробнее'"
                        :colorName="'blue'"
                    />
                </div>
            </div>
        </div>

        <div class="studio">
            <div class="text">
                <div class="info">
                    <h3>Студия с фотофонами</h3>
                    <p>Делайте красивые фотография с интересными фотофонами</p>
                    <Button
                        :text="'Подробнее'"
                    />
                </div>
            </div>
            <div class="img photo"></div>
        </div>
    </section>
</template>

<script>
    import Button from "@/components/Button";

    export default {
        name: "MainStudios",
        components: {
            Button
        }
    }
</script>

<style scoped lang="scss">
    @import "../assets/scss/variables";

    section {
        background-color: $color-1-light;
    }

    h3 {
        font-size: 1.75rem;
        font-weight: 600;
        color: #000000;
        margin: 0;
    }

    p {
        font-size: 1.3rem;
    }

    .studio {
        display: flex;
        align-items: center;

        .img,
        .text {
            width: 50%;
        }

        .text {
            text-align: center;
            padding: 2rem;
        }

        .info {
            display: inline-block;
            max-width: 600px;
        }

        .img {
            height: 300px;

            background-position: center;
            background-size: cover;
            background-repeat: no-repeat;

            &.sound {
                background-image: url('../assets/images/bg/recording-studio.jpg');
            }

            &.photo {
                background-image: url('../assets/images/bg/photo-studio.jpg');
            }
        }
    }

    @media (max-width: 750px) {
        .studio {
            flex-wrap: wrap;

            &:last-child {
                border-top: 1px solid rgba(96, 109, 113, 0.24);
            }
        }

        .img,
        .text {
            width: 100%!important;
        }
    }
</style>