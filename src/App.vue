<template>
  <nav class="navbar_container navbar bg-light">
    <div>
      <a class="navbar_brand navbar-brand">
        <img src="./assets/logo.png" alt="" class="logo_navbar">
        <button class="button " @click="main = true, music = false, military=false, green=false, city=false">GŁÓWNA </button>
        <button class="button" @click="main = false, music = true, military=false, green=false, city=false">MUZYKA </button>
        <button class="button nav_other_title" style=" text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em green;" @click="main = false, music = false, military=false, green=true, city=false">SURVIVAL <br> ZIELONY </button>
        <button class="button nav_other_title" style=" text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em darkred;" @click="main = false, music = false, military=true, green=false, city=false">SURVIVAL <br> MILITARNY </button>
        <button class="button nav_other_title" style=" text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em blue !important;" @click="main = false, music = false, military=false, green=false, city=true">SURVIVAL <br> MIEJSKI </button>
      </a>
    </div>
  </nav>
    <div class="main_choose" style="margin-top: 130px">
      <h1 v-if="main">
         <HelloWorld msg="Wszystko o survivalu"/>
      </h1>
      <h1 v-else-if="music">
         <MusicPage></MusicPage>
      </h1>
      <h1 v-else-if="green">
         <GreenPage></GreenPage>
      </h1>
      <h1 v-else-if="military">
         <MilitaryPage></MilitaryPage>
      </h1>
      <h1 v-else-if="city">
         <CityPage></CityPage>
      </h1>
    </div>
  <a href="javascript:scroll(0,0);"> <img class="arrow" src="@/assets/arrow.png" alt="strzałka"></a>

</template>

<script>
import HelloWorld from './components/WelcomePage.vue'
import MusicPage from "@/components/MusicPage";
import MilitaryPage from "@/components/MilitaryPage";
import GreenPage from "@/components/GreenPage";
import CityPage from "@/components/CityPage";



export default {
  name: 'App',
  components: {
    CityPage,
    GreenPage,
    MilitaryPage,
    MusicPage,
    HelloWorld
  },
  data() {
    return {
      main: true,
      music: true,
      military: true,
      green: true,
      city: true
    }
  },
}
// {
//   (window).scroll(function () {
//       if (this.scrollTop() > 300) ('.arrow').fadeIn();
//       else ('.arrow').fadeOut();
//     }
//     )}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin: 0;
}
.navbar_brand
{
}
.navbar_container
{
  z-index: 1000 ;
  position:fixed;
  width: 100vw;
  background: url("./assets/images.jpg");
  padding: 0!important;
  margin-top: -130px;
}
.main_choose
{
    color: #dcdcdc;
}
.logo_navbar
{
  width: 150px;
}
.button {
  font-size: 30px;
  color: aliceblue;
  text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em #24801a;
  font-family: fantasy;
  background: none;
  border: none;
  margin: 0 1vw 0 1vw;
  /*color: #24801a*/
}
.button:hover
{
  color: #37c225;
}
.nav_other_title
{
  font-size: 20px;
  position: relative;
  top: -20px
}
.arrow
{
  width: 5vw;
  height: 5vw;
  margin-bottom: 30px;
  transition: 1s;
  position: fixed;
	right: 50px;
	bottom: 50px;
}
.arrow:hover
{
  animation: bounce 0.5s infinite linear;
}
@keyframes bounce {
    0% { transform: rotateY(0deg) }
    50% { transform: scale(1.1)}
    100% { transform: rotateY(0deg) }
}
</style>
