<template>
  <nav v-if="display" class="navbar_container navbar bg-light">
    <div>
      <a class="navbar_brand navbar-brand">
        <button v-if="position[1]" class="button_logo" @click="Scrool(),main = true, music = false, military=false, green=false, city=false"> <img src="./assets/logo.png" alt="" class="logo_navbar"> </button>
        <button v-else class="button_logo" style="transform: scale(2); margin: 30px 0 0 30px" @click="Scrool(),main = true, music = false, military=false, green=false, city=false"> <img src="./assets/logo.png" alt="" class="logo_navbar"> </button>
        <button v-if="main" style="color: #37c225;" class="button " @click="Scrool(), main = true, music = false, military=false, green=false, city=false">GŁÓWNA </button>
        <button v-else class="button " @click="Scrool(), main = true, music = false, military=false, green=false, city=false">GŁÓWNA </button>
        <button v-if="music" style="color: #37c225;" class="button" @click="Scrool(), main = false, music = true, military=false, green=false, city=false">MUZYKA </button>
        <button v-else class="button" @click="Scrool(), main = false, music = true, military=false, green=false, city=false">MUZYKA </button>
        <button v-if="green" style="color: green;" class="button nav_other_title1" @click="Scrool(), main = false, music = false, military=false, green=true, city=false">SURVIVAL <br> ZIELONY </button>
        <button v-else class="button nav_other_title1" @click="Scrool(), main = false, music = false, military=false, green=true, city=false">SURVIVAL <br> ZIELONY </button>
        <button v-if="military" style="color: darkred;" class="button nav_other_title2" @click="Scrool(), main = false, music = false, military=true, green=false, city=false">SURVIVAL <br> MILITARNY </button>
        <button v-else class="button nav_other_title2" @click="Scrool(), main = false, music = false, military=true, green=false, city=false">SURVIVAL <br> MILITARNY </button>
        <button v-if="city" style="color: blue;" class="button nav_other_title3" @click="Scrool(), main = false, music = false, military=false, green=false, city=true">SURVIVAL <br> MIEJSKI </button>
        <button v-else class="button nav_other_title3" @click="Scrool(), main = false, music = false, military=false, green=false, city=true">SURVIVAL <br> MIEJSKI </button>
<!--        <button class="button" @click="czy=!czy">zmiana</button>-->
<!--        {{czy}}{{test2}}-->
      </a>
    </div>
  </nav>
  <nav v-else class="navbar_container navbar bg-light">
    <section class="navbar_brand navbar-brand">
    <button class="button_logo" @click="Scrool(),main = true, music = false, military=false, green=false, city=false"> <img src="./assets/logo.png" alt="" class="logo_navbar"> </button>

    <input id="menu-toggle" type="checkbox" />
    <label class='menu-button-container' for="menu-toggle">
    <div class='menu-button'></div>
  </label>
    <ul class="menu">
        <li><button class="button " @click="Scrool(), main = true, music = false, military=false, green=false, city=false">GŁÓWNA </button></li>
        <li><button class="button" @click="Scrool(), main = false, music = true, military=false, green=false, city=false">MUZYKA </button></li>
        <li><button class="button nav_other_title1" @click="Scrool(), main = false, music = false, military=false, green=true, city=false">SURVIVAL ZIELONY </button></li>
        <li><button class="button nav_other_title2" @click="Scrool(), main = false, music = false, military=true, green=false, city=false">SURVIVAL MILITARNY </button></li>
        <li><button class="button nav_other_title3" @click="Scrool(), main = false, music = false, military=false, green=false, city=true">SURVIVAL MIEJSKI </button></li>
    </ul>
  </section>
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

    <a v-if=position[1] href="javascript:scroll(0,0);">
      <img class="arrow" src="@/assets/arrow.png" alt="strzałka">
      <img v-if="military" class="arrow" style="background-color: darkred" src="@/assets/arrow.png" alt="strzałka">
      <img v-if="city" class="arrow" style="background-color: blue" src="@/assets/arrow.png" alt="strzałka">
    </a>

  <FooterLine :info="military" :info2="city" @first="MainPage" @second="MusicPage"  @third="GreenPage" @fourth="MilitaryPage" @fifth="CityPage"> </FooterLine>

</template>

<script>
import HelloWorld from './components/WelcomePage.vue'
import MusicPage from "@/components/MusicPage";
import MilitaryPage from "@/components/MilitaryPage";
import GreenPage from "@/components/GreenPage";
import CityPage from "@/components/CityPage";
import FooterLine from "@/components/Footer";
import WinowScrollPosition from "./window-scroll-position";

export default {
  name: 'App',
  mixins:[WinowScrollPosition('position')],
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
      music: false,
      military: false,
      green: false,
      city: false,
      display: true,
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
    onResize() {
      if (window.innerWidth < 900) {
          this.display = false;
        } else {
          this.display = true;
        }
    }
  },

    created() {
      window.addEventListener('resize', this.onResize)
    },
    beforeUnmount() {
      window.removeEventListener('resize', this.onResize)
    }
    // Disappearing()
    // {
    //     if(scroll(0,300))
    //     {
    //       this.disappearing_bool=true;
    //     }
    // }
    // test4(e) {
    //   this.czy.push(e);
    //   this.test5=e;
    //   },
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
  height: 130px;
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
  transition: 1s;
  margin-right: 30px;
}

.button {
  font-size: 30px;
  color: aliceblue;
  text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em #24801a;
  font-family: fantasy;
  background: none;
  border: none;
  margin: 50px 1vw 0 1vw;
  /*color: #24801a*/
  vertical-align: top;
}
.button:hover
{
  color: #37c225;
}
.nav_other_title1
{
  font-size: 20px;
  position: relative;
  top: -10px;
  text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em green;
}
.nav_other_title2
{
  font-size: 20px;
  position: relative;
  top: -10px;
  text-shadow: 0 0 0.2em darkred, 0 0 0.2em #e0c708, 0 0 0.2em darkred;
}
.nav_other_title3
{
  font-size: 20px;
  position: relative;
  top: -10px;
  text-shadow: 0 0 0.2em blue, 0 0 0.2em #e0c708, 0 0 0.2em blue;
}
.nav_other_title1:hover
{
  color: green;
}
.nav_other_title2:hover
{
  color: darkred;
}
.nav_other_title3:hover
{
  color: blue;
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
  0% {
    transform: rotateY(0deg)
  }
  50% {
    transform: scale(1.1)
  }
  100% {
    transform: rotateY(0deg)
  }
}

/*------------Burger Menu--------*/

  .menu {
    display: flex;
    list-style-type: none;
    margin: 0;
    padding: 0;
    position: absolute;
    top: 0;
    left: 0;
    flex-direction: column;
    width: 100%;
    justify-content: center;
    align-items: center;
    }

  .menu > li {
    margin: 0 1rem;
    overflow: hidden;
  }

  .menu-button-container {
    display: flex;
    height: 100%;
    width: 30px;
    cursor: pointer;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 0;
    right: 30px;
    z-index: 100;
  }

  #menu-toggle {
    display: none;
  }

  .menu-button,
  .menu-button::before,
  .menu-button::after {
    display: block;
    background-color: white;

    position: absolute;
    height: 4px;
    width: 30px;

    transition: transform 400ms cubic-bezier(0.23, 1, 0.32, 1);
    border-radius: 2px;
  }

  .menu-button::before {
    content: '';
    margin-top: -8px;
  }

  .menu-button::after {
    content: '';
    margin-top: 8px;
  }

  #menu-toggle:checked + .menu-button-container .menu-button::before {
    margin-top: 0px;
    transform: rotate(405deg);
  }

  #menu-toggle:checked + .menu-button-container .menu-button {
    background: rgba(255, 255, 255, 0);
  }

  #menu-toggle:checked + .menu-button-container .menu-button::after {
    margin-top: 0px;
    transform: rotate(-405deg);
  }
  #menu-toggle ~ .menu li {
    height: 0;
    margin: 0;
    padding: 0;
    border: 0;
    transition: height 400ms cubic-bezier(0.23, 1, 0.32, 1);
  }
  #menu-toggle:checked ~ .menu li {
    border: 1px solid #333;
    height: 4em;
    padding: 0.5em;
    transition: height 400ms cubic-bezier(0.23, 1, 0.32, 1);
  }
  .menu > li {
    display: flex;
    justify-content: center;
    margin: 0;
    padding: 0.5em 0;
    width: 100%;
    color: white;
    background-color: #222;
  }
  .menu > li:not(:last-child) {
    border-bottom: 1px solid #444;
  }


  /*-----------------------------------------------------------------------*/
  @media screen and (max-width: 850px) {
    .nav_other_title1 {
      top: 0;
      font-size: 30px;
    }

    .nav_other_title2 {
      top: 0;
      font-size: 30px;
    }

    .nav_other_title3 {
      top: 0;
      font-size: 30px;
    }

    .arrow {
      display: none;
    }

    .button {
      margin: 0px 1vw 0 1vw;
    }
  }


</style>
