<template>
  <div class="welcome_page">
    <h1>{{ msg }}</h1>
     <h2>Zacznij swoją przygodę z survivalem! </h2>
      <div class="description">
        <i style="text-shadow: 0 0 0.2em #000, 0 0 0.2em #000, 0 0 0.2em #000;" >"Mianem <b style="text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em #24801a;">survivalu</b> (lub surwiwalu) określa się sztukę przetrwania w trudnych warunkach. Jest to swego rodzaju samoratownictwo,
        czyli radzenie sobie w specyficznym scenariuszu,
        np. klęski żywiołowej, wojny, wypadku, zagubienia na odludziu itd. Dotyczy to ekstremalnych sytuacji i to nie tylko w dziczy, ale i w mieście (np. podczas blackoutu).
        Survival obejmuje wiele dziedzin. Zawierają się w nim zarówno umiejętności praktyczne (np. rozpalanie ognia),
        pozyskiwanie wiedzy (np. o gatunkach roślin lub wskazówkach nawigacyjnych), a także kwestie mentalne.
        Opanowanie strachu, emocji, lęku wysokości czy adrenaliny stanowi ważną część treningu survivalowego."
        </i>
      </div>
    <div class="line"></div>
  </div>
  <section class="kinds">
    <div> Rodzaje Survivalu</div>
    <div>
      <div class="description_list"> Survival występuje w wielu odmianach, które można ukształtować dla własnych potrzeb.
        Ze względu na charakter aktywności surwiwalowej wyróżnia się zazwyczaj trzy główne odmiany:
      </div>
      <ul class="list">
        <li class="list_item" style="text-shadow: 0 0 0.2em darkred;">
          <button class="list_item_title" style="text-shadow: 0 0 0.2em darkred;" @click="main = false, music = false, military=true, green=false, city=false"><b>survival militarny</b></button>
          – celem jest, podobnie jak w wojsku, nabycie i utrzymanie umiejętności pozwalających na zachowanie sprawności
          i życia dla wykonania ustalonego zadania. Ten element decyduje o charakterze szkolenia. Mogą tu występować formy rekreacyjne,
          ale survival militarny może być traktowany jako faktyczne utrzymywanie wojskowej sprawności na wypadek działań wojennych
        </li>
        <li class="list_item" style="text-shadow: 0 0 0.2em green;">
          <button class="list_item_title" style="text-shadow: 0 0 0.2em green;"><b>survival zielony</b></button> – celem jest nabycie i utrzymanie umiejętności pozwalających na samowystarczalną egzystencję w warunkach przebywania poza cywilizacją.
          Istnieje tu duży związek z naturą. Ten rodzaj survivalu nastawiony jest silnie na rekreację, ale – w wersji rozwiniętej
          – przygotowuje też do działań w warunkach zagrożeń podczas klęsk żywiołowych, katastrof komunikacyjnych, itp.
        </li>
        <li class="list_item" style="  text-shadow: 0 0 0.2em blue;">
          <button class="list_item_title" style="text-shadow: 0 0 0.2em blue;"><b>survival miejski</b></button> – celem survivalu miejskiego jest działanie samowystarczalne w warunkach metropolii,
          a więc szukania możliwości przetrwania w zagęszczeniu uwarunkowań społecznych.
          Ten rodzaj survivalu stawia nacisk na doświadczanie własnych możliwości i elementy poznawcze.

        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 70px 0 0;
  font-family: fantasy;
  font-size: 60px;
  text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em #24801a;
  transition: 1s;
}
h1:hover
{
  transform: scale(1.2);
  cursor: pointer;
}
h2{

  margin: 20px;
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
  background: url("../assets/Background.jpg");
  background-size: cover;
  height: 80vh;
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
.kinds
{
  background-image: url("../assets/wood.jpg");
  color: white;
  padding: 30px 20vw 40px 20vw;
  text-align: justify;
  flex-direction: column;
  align-items: center;
  margin-bottom: -10px;
}
.description_list
{
  font-size: 25px;
  background: linear-gradient( to right, red, orange);
  border-radius: 30px;
  padding: 10px;
  margin-top: 20px;
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
  text-transform: uppercase;
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


}
</style>
