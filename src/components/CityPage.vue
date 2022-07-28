<template>
  <div class="container_city ">
    <div class="title w3-animate-right">
    Survival Miejski
    </div>
    <div class="main_description w3-animate-left">
        Żyjemy w względnych czasach pokoju, lecz nie trzeba wiele, by gospodarka i całe państwa upadły jak zamek z kart. Epidemia Covid-19 pokazała nam jak szybko ludzie popadają w panikę
      i co dzieje się ze społeczeństwem. Survivalowcy zwani rownież "Prepersami" muszą być gotowi na taką sytuację i mieć sprzęt niezbędny do przeżycia w czasie nawet największej klęski.
      Aby przeżyć, nalezy być przygotowanym. Należy pamiętać że z takich lub innych względów nie możesz przeczekać całego zamieszania w domu.
      Być może „stan wyjątkowy” będzie trwał zbyt długo i kruczące się zapasy zmuszą Cię do wyjścia. Albo Twój dom z jakichś względów nie będzie się nadawał do dalszego zamieszkiwania.
      Powodów może być wiele, po prostu musisz byc gotowy wyjść, eksplorować, zdobywać zasoby lub uciekać.
      W dalszej części umieszczona jest lista rzeczy które warto mieć pod ręką.
    </div>
    <div class="choose_buttons">
      <button class="button_city_page"  @click="selected_topic='ODZIEŻ'">ODZIEŻ </button>
      <button class="button_city_page"  @click="selected_topic='BROŃ'">BROŃ </button>
      <button class="button_city_page"  @click="selected_topic='ŻYWOŚĆ'">ŻYWOŚĆ </button>
      <button class="button_city_page"  @click="selected_topic='ELEKTRONIKA'">ELEKTRONIKA </button>
      <button class="button_city_page"  @click="selected_topic='SCHRONIENIE'">SCHRONIENIE </button>
      <button class="button_city_page"  @click="selected_topic='INNE'">INNE </button>
    </div>
    <div v-if="selected_topic=='ODZIEŻ'">
      <ClothesPage class="w3-animate-top"></ClothesPage>
    </div>
    <div v-else-if="selected_topic=='BROŃ'">
      <WeaponPage class="w3-animate-top"></WeaponPage>
    </div>
    <div v-else-if="selected_topic=='ŻYWOŚĆ'">
      <FoodPage class="w3-animate-top"></FoodPage>
    </div>
    <div v-else-if="selected_topic=='ELEKTRONIKA'">
      <ElectronicPage class="w3-animate-top"></ElectronicPage>
    </div>
    <div v-else-if="selected_topic=='SCHRONIENIE'">
      <ShelterPage class="w3-animate-top"></ShelterPage>
    </div>
    <div v-else-if="selected_topic=='INNE'">
      <OtherPage class="w3-animate-top"></OtherPage>
    </div>

  </div>
</template>

<script>

import ClothesPage from "@/components/CityPage_components/Clothes";
import ElectronicPage from "@/components/CityPage_components/Electronics";
import ShelterPage from "@/components/CityPage_components/Shelter";
import WeaponPage from "@/components/CityPage_components/Weapon";
import FoodPage from "@/components/CityPage_components/Food";
import OtherPage from "@/components/CityPage_components/Other";
export default {
  name: "CityPage",
  components: {OtherPage, FoodPage, WeaponPage, ShelterPage, ElectronicPage, ClothesPage},
  data(){
    return{
      selected_topic:'ODZIEŻ',
      topics:[
        {topic:'ODZIEŻ'},
        {topic:'BROŃ'},
        {topic:'ŻYWOŚĆ'},
        {topic:'ELEKTRONIKA'},
        {topic:'SCHRONIENIE'},
        {topic:'INNE'}
      ]

    }
  }
}


</script>

<style scoped>
.container_city
{
  background-size: cover;
  background-image: linear-gradient(rgba(255,255,255,0.5), rgba(255,255,255,0.5)), url("../assets/city_survival.jpg");
  min-height: 1000px;
  margin-bottom: -10px;
  padding-bottom: 200px;
}
.title
{
  color: blue;
  padding: 30px 10px;
  font-family: fantasy;
  letter-spacing: 2px;
}
.main_description{
  font-size: 20px;
  text-align: justify;
  list-style: none;
  padding: 20px 10vw 20px 10vw;
  color: black;
}
.button_city_page
{
  padding: 15px 25px;
  margin: 0 20px 0 20px;
  font-size: 24px;
  text-align: center;
  cursor: pointer;
  outline: none;
  color: #fff;
  background-color: blue;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}
.button_city_page:hover
{
  background-color: midnightblue;
}
.button_city_page:active {
  background-color: midnightblue;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
.button_city_page:focus {
  background-color: dodgerblue;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
@media screen and (max-width:1200px)
{
  .choose_buttons
  {
    display: flex;
    flex-direction: column;
    align-items: center;

  }
  .button_city_page
  {
    width: 60vw;
    margin-bottom: 30px;
  }

}

@media screen and (max-width: 850px ){
    .container_city
  {
    padding-bottom: 300px;
  }
}


</style>