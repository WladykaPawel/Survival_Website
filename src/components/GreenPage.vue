<template>
  <div class="container_green">
    <div class="title w3-animate-right">
      Survival Zielony
    </div>
    <div class="choose_information w3-animate-left ">Wybierz intereującą Cię tematykę survivalowową</div>
    <select class="choose" v-model="selected_topic">
      <option class="options" v-for="topic in topics" :key="topic.id">
        {{ topic.topic }}
      </option>
    </select>
    <div class="main_container w3-animate-top" v-if="selected_topic=='Przygotowania'">
      <PreparationPage></PreparationPage>
    </div>
    <div class="main_container w3-animate-top" v-if="selected_topic=='Broń'">
      <WeaponPage></WeaponPage>
    </div>
    <div class="main_container w3-animate-top" v-if="selected_topic=='Miejsce do spania'">
      <PlaceToSleepPage></PlaceToSleepPage>
    </div>
    <div class="main_container w3-animate-top" v-if="selected_topic=='Zdobywanie jedzenia'">
      <GettingFoodPage></GettingFoodPage>
    </div>
    <div class="main_container w3-animate-top" v-if="selected_topic=='Ogień i Ogniska'">
      C.D.N...
    </div>
    <div class="main_container w3-animate-top" v-if="selected_topic=='BHP i Pierwsza Pomoc'">
      C.D.N...
    </div>

  </div>
</template>

<script>
import PreparationPage from "@/components/GreenPage_components/Preparation";
import WeaponPage from "@/components/GreenPage_components/Weapon";
import PlaceToSleepPage from "@/components/GreenPage_components/PlaceToSleep";
import GettingFoodPage from "@/components/GreenPage_components/GettingFood";
export default {
  name: "GreenPage",
  components: {GettingFoodPage, PlaceToSleepPage, WeaponPage, PreparationPage},
  data(){
    return{
      selected_topic:'Przygotowania',
      topics:[
        {topic:'Przygotowania'},
        {topic:'Broń'},
        {topic:'Miejsce do spania'},
        {topic:'Zdobywanie jedzenia'},
        {topic:'Ogień i Ogniska'},
        {topic:'BHP i Pierwsza Pomoc'}
      ]
    }
  }
}
</script>

<style scoped>
.container_green
{
  background-size: cover;
  background-image: linear-gradient(rgba(255,255,255,0.5), rgba(255,255,255,0.5)), url("../assets/green_survival.jpg");
  min-height: 2000px;
  margin-bottom: -10px;
  padding-bottom: 200px;
}
.title
{
  color: green;
  padding: 30px 10px;
  font-family: fantasy;
  letter-spacing: 2px;
}

.choose
{
  font-size: 20px;
  color: white;
  border-radius: 5px;
  width: 30vw;
  padding: 12px;
  background: url("../assets/Music_background.jpg");

}
.options
{
  padding: 40px;
  border-radius: 10px;
  background-color: #4c4c4c;
}
.choose_information
{
  color: darkgreen;
  padding-bottom: 50px;
}
.main_container
{
	display: flex;
  flex-direction: column;
	align-items: center;
  justify-content: center;
  margin: 30px 6vw 0 6vw;
  color: #24801a;
}

@media screen and (max-width: 800px){
  .choose {
    width: 60vw;
  }

}

</style>