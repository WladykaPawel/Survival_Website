<template>
  <nav class="navbar_container navbar bg-light">
    <div>
      <a class="navbar_brand navbar-brand">
        <button class="button_logo" @click="Scrool(),main = true, music = false, military=false, green=false, city=false"> <img src="./assets/logo.png" alt="" class="logo_navbar"> </button>
        <button class="button " @click="Scrool(), main = true, music = false, military=false, green=false, city=false">GŁÓWNA </button>
        <button class="button" @click="Scrool(), main = false, music = true, military=false, green=false, city=false">MUZYKA </button>
        <button class="button nav_other_title" style=" text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em green;" @click="Scrool(), main = false, music = false, military=false, green=true, city=false">SURVIVAL <br> ZIELONY </button>
        <button class="button nav_other_title" style=" text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em darkred;" @click="Scrool(), main = false, music = false, military=true, green=false, city=false">SURVIVAL <br> MILITARNY </button>
        <button class="button nav_other_title" style=" text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em blue" @click="Scrool(), main = false, music = false, military=false, green=false, city=true">SURVIVAL <br> MIEJSKI </button>
<!--        <button class="button" @click="czy=!czy">zmiana</button>-->
<!--        {{czy}}{{test2}}-->
      </a>
    </div>
  </nav>
    <div class="main_choose" style="margin-top: 130px">
      <h1 v-if="main">
        <HelloWorld @first="GreenPage" @second="MilitaryPage" @third="CityPage" msg="Wszystko o survivalu"></HelloWorld>
<!--          <HelloWorld :test="czy" @add="()=> czy=!czy " msg="Wszystko o survivalu"></HelloWorld>-->
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

    <a href="javascript:scroll(0,0);">
      <img class="arrow" src="@/assets/arrow.png" alt="strzałka">
    </a>

  <FooterLine  @first="MainPage" @second="MusicPage"  @third="GreenPage" @fourth="MilitaryPage" @fifth="CityPage"> </FooterLine>

</template>

<script>
import HelloWorld from './components/WelcomePage.vue'
import MusicPage from "@/components/MusicPage";
import MilitaryPage from "@/components/MilitaryPage";
import GreenPage from "@/components/GreenPage";
import CityPage from "@/components/CityPage";
import FooterLine from "@/components/Footer";



export default {
  name: 'App',
  components: {
    FooterLine,
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
      city: true,
      test: false,
      disappearing_bool:false
    }
  },
  methods:
  {
    MainPage()
    {
      this.Scrool();
      this.main= true;
      this.music= false;
      this.military= false;
      this.green= false;
      this.city= false;

    },
    MusicPage()
    {
      this.Scrool();
      this.main= false;
      this.music= true;
      this.military= false;
      this.green= false;
      this.city= false;

    },
    GreenPage()
    {
      this.Scrool();
      this.main= false;
      this.music= false;
      this.military= false;
      this.green= true;
      this.city= false;

    },
    MilitaryPage()
    {
      this.Scrool();
      this.main= false;
      this.music= false;
      this.military= true;
      this.green= false;
      this.city= false;
    },
    CityPage()
    {
      this.Scrool();
      this.main= false;
      this.music= false;
      this.military= false;
      this.green= false;
      this.city= true;
    },
    Scrool()
    {
      scroll(0,0);
    },
    Disappearing()
    {
        if(scroll(0,300))
        {
          this.disappearing_bool=true;
        }
    }
    // test4(e) {
    //   this.czy.push(e);
    //   this.test5=e;
    //   },

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
  margin: -10px;
}
.button_logo
{
  background: none;
  border: none;


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
  width: 7vh;
  height: 7vh ;
  margin-bottom: 30px;
  transition: 1s;
  position: fixed;
	right: 50px;
	bottom: 30px;
  background: #24801a;
  border-radius: 300px;
  padding: 10px;
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
