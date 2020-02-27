<template>
  <div id="app">

    <!--  Главная шапка  -->
    <MainHeader />

    <!--  Афиша  -->
    <MainPosters />

    <!--  Дворец культуры  -->
    <MainAboutPalace />

    <!--  О зале Дворца культуры  -->
    <MainAboutAssemblyHall />

    <!--  О конференц-зале  -->
    <MainAboutConferenceHall />

    <!--  О студиях  -->
    <MainStudios />

    <!--  Аренда  -->
    <MainRent />

    <!--  Контакты  -->
    <MainContacts />

    <!--  Подвал  -->
    <MainFooter />

  </div>
</template>

<script>
import MainHeader from "@/components/MainHeader";
import MainPosters from "@/components/MainPosters";
import MainAboutPalace from "@/components/MainAboutPalace";
import MainAboutAssemblyHall from "@/components/MainAboutAssemblyHall";
import MainAboutConferenceHall from "@/components/MainAboutConferenceHall";
import MainStudios from "@/components/MainStudios";
import MainRent from "@/components/MainRent";
import MainContacts from "@/components/MainContacts";
import MainFooter from "@/components/MainFooter";

export default {
  name: 'App',
  components: {
    MainHeader,
    MainPosters,
    MainAboutPalace,
    MainAboutAssemblyHall,
    MainAboutConferenceHall,
    MainStudios,
    MainRent,
    MainContacts,
    MainFooter
  }
}
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
  }

  html {
    font-size: 16px;
  }

  body {
    font-family: 'Exo 2',serif;
    margin: 0;
    /*color: rgba(0,0,0,0.8);*/
    color: #3e3c3c;
  }

  h2 {
    margin: 3rem 0 3.5rem 0;
    font-family: 'Lobster',serif;
    font-size: 3rem;
    text-align: center;
  }

  .wrapper {
    width: 100%;
    max-width: 1024px;
    margin: 0 auto;
    padding: 0 1rem;
  }

  .cntr {
    text-align: center;
  }

  .mtb2 {
    margin-top: 2rem;
    margin-bottom: 2rem;
  }
  .mtb3 {
    margin-top: 3rem;
    margin-bottom: 3rem;
  }

  .w50 {
    width: 50%;
  }
</style>
