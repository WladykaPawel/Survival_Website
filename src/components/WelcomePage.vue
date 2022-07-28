<template>
  <div class="welcome_page">
    <h1 class="w3-animate-zoom">{{ msg }}</h1>
     <h2 class="w3-animate-zoom">Zacznij swoją przygodę z survivalem! </h2>
      <div class="description w3-animate-top">
        <i style="text-shadow: 0 0 0.2em #000, 0 0 0.2em #000, 0 0 0.2em #000;" >"Mianem <b style="text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em #24801a;">survivalu</b> (lub surwiwalu) określa się sztukę przetrwania w trudnych warunkach. Jest to swego rodzaju samoratownictwo,
        czyli radzenie sobie w specyficznym scenariuszu,
        np. klęski żywiołowej, wojny, wypadku, zagubienia na odludziu itd. Dotyczy to ekstremalnych sytuacji i to nie tylko w dziczy, ale i w mieście (np. podczas blackoutu).
        Survival obejmuje wiele dziedzin. Zawierają się w nim zarówno umiejętności praktyczne (np. rozpalanie ognia),
        pozyskiwanie wiedzy (np. o gatunkach roślin lub wskazówkach nawigacyjnych), a także kwestie mentalne.
        Opanowanie strachu, emocji, lęku wysokości czy adrenaliny stanowi ważną część treningu survivalowego."
        </i>
      </div>
    <div class="line"></div>
    <div class="test_slider"></div>
  </div>
  <section class="kinds">
    <div> Rodzaje Survivalu</div>
<!--    {{test}}-->
<!--    {{test2}}-->
<!--    <button class="button" @click="test2!=test2, $emit('add', test2)">zmiana</button>-->
    <div>
      <div class="description_list"> Survival występuje w wielu odmianach, które można ukształtować dla własnych potrzeb.
        Ze względu na charakter aktywności surwiwalowej wyróżnia się zazwyczaj trzy główne odmiany:
      </div>
      <ul class="list">
        <li class="list_item" style="text-shadow: 0 0 0.2em green;">
          <button class="list_item_title" @click="ChangePageGreen" style="text-shadow: 0 0 0.2em green;"><b style="text-transform: uppercase; color: black">survival zielony</b>
            – celem jest nabycie i utrzymanie umiejętności pozwalających na samowystarczalną egzystencję w warunkach przebywania poza cywilizacją.
          Istnieje tu duży związek z naturą. Ten rodzaj survivalu nastawiony jest silnie na rekreację, ale – w wersji rozwiniętej
          – przygotowuje też do działań w warunkach zagrożeń podczas klęsk żywiołowych, katastrof komunikacyjnych, itp.
            </button>
        </li>
        <li class="list_item" style="text-shadow: 0 0 0.2em darkred;">
          <button class="list_item_title" @click="ChangePageMilitary" style="text-shadow: 0 0 0.2em darkred;"><b style="text-transform: uppercase; color: black">survival militarny</b>
          – celem jest, podobnie jak w wojsku, nabycie i utrzymanie umiejętności pozwalających na zachowanie sprawności
          i życia dla wykonania ustalonego zadania. Ten element decyduje o charakterze szkolenia. Mogą tu występować formy rekreacyjne,
          ale survival militarny może być traktowany jako faktyczne utrzymywanie wojskowej sprawności na wypadek działań wojennych
          </button>
        </li>
        <li class="list_item" style="  text-shadow: 0 0 0.2em blue;">
          <button class="list_item_title" @click="ChangePageCity" style="text-shadow: 0 0 0.2em blue;"><b style="text-transform: uppercase; color: black">survival miejski</b>
            – celem survivalu miejskiego jest działanie samowystarczalne w warunkach metropolii,
          a więc szukania możliwości przetrwania w zagęszczeniu uwarunkowań społecznych.
          Ten rodzaj survivalu stawia nacisk na doświadczanie własnych możliwości i elementy poznawcze.
            </button>

        </li>
      </ul>
    </div>
  </section>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    // test: Boolean
  },
  methods:
  {
    ChangePageGreen()
    {
      this.$emit('first', this.green)
    },
    ChangePageMilitary()
    {
      this.$emit('second', this.military)
    },
    ChangePageCity()
    {
      this.$emit('third', this.city)
    }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 70px 0 0 0 ;
  font-family: fantasy;
  font-size: 55px;
  text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em #24801a;
  transition: 1s;
  animation: anime 15s infinite linear;
}
h1:hover
{
  animation: anime 5s infinite linear;
}

@keyframes anime {
  0% {
    transform: scale(1.1);
    color: #37c225;
  }
  25% {
    transform: scale(1);
    color: white;
  }
  50% {
    transform: scale(1.1);
    color: #37c225;
  }
  75% {
    transform: scale(1);
    color: white;
  }
  100% {
    transform: scale(1.1);
    color: #37c225;
  }
  /*75% {*/
  /*  transform: rotateY(180deg);*/
  /*}*/
  /*100% {*/
  /*  transform: rotateY(-180deg);*/
  /*}*/

}
h2{

  margin: 20px;
  font-family: fantasy;
}

a {
  color: #42b983;
}
.welcome_page
{
  display: flex;
  flex-direction: column;
  align-items: center;
  flex-wrap: wrap;
  /*background: url("../assets/Background.jpg");*/
  background: url("../assets/giphy.gif");
  background-size: cover;
  height: 100vh;
}
.description
{
  text-align: justify;
  align-items: center;
  color: aliceblue;
  overflow: auto;
  text-overflow: ellipsis;
  max-height: 250px;
  padding: 10px;
  max-width: 1400px;
  margin: 0 30px 0 30px;
  font-size: 20px;
  backdrop-filter: sepia(100%);
}
.line
{
  background-color: #e0c708;
  width: 75vw;
  height: 3px;
  margin: 80px 10px 0 10px;
}

.test_slider
{
  margin-top: 20px;
  width: 400px;
  height: 250px;
  animation: slider 20s infinite linear;
  background-size: cover;
}

@keyframes slider {
  0%{
    background:url("../assets/City_survival/odziez.jpg");
    border-radius: 50px;
    background-position: center;
    background-size: cover;
  }
  25%{
    background:url("../assets/City_survival/inne.jpg");
    border-radius: 10px;
    background-position: center;
    background-size: cover;
  }
  50%{
    background:url("../assets/City_survival/schronienie.jpg");
    border-radius: 10px;
    background-position: center;
    background-size: cover;
  }
  75%{
    background:url("../assets/City_survival/bron.jpg");
    border-radius: 50px;
    background-position: center;
    background-size: cover;
  }
  100%{
    background:url("../assets/City_survival/odziez.jpg");
    border-radius: 50px;
    background-position: center;
    background-size: cover;
  }

}

.kinds
{
  background-image: linear-gradient(rgba(255,255,255,0.2), rgba(255,255,255,0.2)), url("../assets/background-burnt-damaged-grunge.jpg");
  background-size: cover;
  color: white;
  padding: 30px 15vw 300px 15vw;
  text-align: justify;
  flex-direction: column;
  align-items: center;
  margin-bottom: -10px;
}
.description_list
{
  font-size: 25px;
  border-radius: 30px;
  padding: 15px;
  transition: 2s;
  margin: 30px 6vw 10px 6vw;
  animation: change 0.5s infinite linear;
}
@keyframes change{
  0%{background: linear-gradient( 0deg, darkgreen, green);}
  25%{background: linear-gradient( 45deg, darkgreen, green);}
  25%{background: linear-gradient( 90deg, darkgreen, green);}
  37%{background: linear-gradient( 135deg, darkgreen, green);}
  50%{background: linear-gradient( 180deg, darkgreen, green);}
  62%{background: linear-gradient( 225deg, darkgreen, green);}
  75%{background: linear-gradient( 270deg, darkgreen, green);}
  87%{background: linear-gradient( 315deg, darkgreen, green);}
  100%{background: linear-gradient( 360deg, darkgreen, green);}
}
.list
{
  font-size: 26px;
  padding: 20px 50px 0 50px;
  text-align: justify;
}
.list_item
{
  padding: 10px;
}
.list_item_title
{
  border: none;
  background: none;
  text-align: justify;
  color: white;
}
.list_item_title:hover
{
  color: black;
  cursor: pointer ;
}

@media screen and (max-width:1050px){
  .line
  {
     margin: 30px 0 0 0;
  }
  .welcome_page
  {
    height: 100vh;
  }
  .description {
    font-size: 16px;
  }
  .description_list
  {
    font-size: 20px;
    margin: 30px -3vw 10px -3vw;
  }
  .list
  {
    font-size: 18px;
    padding: 20px 10px 0 10px;
  }
  .test_slider
  {
    display: none;
  }
}
</style>
