<template>
  <div class="Other_desc">
    INNE
    <div class="Other_main">
      <ul class="description">
        <img class="image" src="@/assets/City_survival/inne.jpg" alt="inne">
        <li class="items">
          <h1 class="title_1">Plecak</h1>
          Powinien być dopasowany do sylwetki, wytrzymały, pakowny. Ale też nie za duży – w mieście często trzeba przeciskać się przez wąskie przejścia, niewielkie okna lub zawalone gruzem korytarze.
        </li>
        <li class="items">
          <h1 class="title_1">Medykamenty</h1>
           Do swojej podręcznej apteczki wsadź: leki przeciwbólowe i
          przeciwgorączkowe (ibuprofen, paracetamol), przeciwbiegunkowe
          (stoperan, węgiel), bandaże i plastry, kompresy, stazę
          (choć tę lepiej nosić gdzieś pod ręką), opaski uciskowe, nożyczki,
          mocny alkohol (dezynfekuje i… podnosi morale), środki na oparzenia,
          jednorazowe rękawiczki, może coś na komary.
        </li>
        <li class="items">
          <h1 class="title_1">Mapa miasta i kompas</h1>
          Mimo znajomości miasta...Przezorny zawsze ubezpieczony.
        </li>
        <li class="items">
          <h1 class="title_1">Krzesiwo, zapalniczki, zapałki sztormowe</h1>
          Jeszcze jeden obowiązkowy punkt programu. Ogień pozwala coś upichcić, zagrzać (i wysterylizować) wodę, wysuszyć ciuchy i ogrzać się. Jest więc podstawą każdego survivalu.
        </li>
        <li class="items">
          <h1 class="title_1">Narzędzia</h1>
          - Niewielkie nożyce do cięcia prętów.
          - Kombinerki, śrubokręty, multitoole.
          - Mały łom.
          - Składana piłka.
        </li>
        <li class="items">
          <h1 class="title_1">Okulary ochronne</h1>
          Chronią oczy nie tylko przed łuskami.
        </li>
        <li class="items">
          <h1 class="title_1">Maseczka</h1>
          Nie, nie na COVIDA-a. Raczej „na” pył i dym.
        </li>
        <li class="items">
          <h1 class="title_1">Bransoleta z paracordu</h1>
          Kilkanaście metrów mocnego sznurka potrafi uratować tyłek.
        </li>
        <li class="items">
          <h1 class="title_1">Notes</h1>
         Zapisz w nim adresy i telefony. Tak na wszelki wypadek. Możesz też zacząć prowadzić dziennik. W kryzysowych sytuacjach może to pomóc zachować równowagę psychiczną.
        </li>
        <li class="items">
          <h1 class="title_1">Prezerwatywy</h1>
          Można w nich np. transportować wodę.
        </li>
        <li class="items">
          <h1 class="title_1">Szara taśma</h1>
          Wiadoma sprawa. Naprawisz nią nawet prom kosmiczny.
        </li>
        <li class="items">
          <h1 class="title_1">Podgrzewacze</h1>
         W parze z prezerwatywami jest to kluczowy elementy romantycznego, postapokaliptycznego: <i>rendez-vous</i> A mówiąc poważnie, stanowią awaryjne źródło światła i ciepła.
        </li>
        <li class="items">
          <h1 class="title_1">Gwizdek</h1>
         W razie problemów będziesz w stanie wezwać pomoc lub przekazać swoje położenie.
        </li>
      </ul>

    </div>
  </div>
</template>

<script>
export default {
  name: "OtherPage"
}
</script>

<style scoped>
.Other_desc
{
  color: blue;
  padding: 50px 20px 20px 20px;
}
.Other_main
{
  color: #4c4c4c;
  font-size: 25px;
  padding: 20px 10vw 20px 10vw;
  text-align: justify;
}
.description
{

  color: #4c4c4c;
  font-size: 20px;
  text-align: justify;
  padding: 0 10vw 10px 10vw;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.title_1
{
  color: blue;
  font-size: 30px;
  padding: 10px;
}
.items
{
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #FFFFFF;
  border-radius: 10px;
  margin-bottom: 20px;
  padding: 0 10vw 50px 10vw;
  min-width: 70vw;

}
.items:hover
{
  background: linear-gradient(to right, white, lightblue);
}
.image
{
  width: 50vw;
  align-items: center;
  transition: 1s;
  border-radius: 50px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.5), 0 6px 20px 0 rgba(0, 0, 0, 0.5);
  margin-bottom: 70px;
}
.image:hover
{
  cursor: pointer;
  animation: shake 1s infinite linear;
}
@keyframes shake{
  25% {transform: scale(1.01)}
  75% {transform: scale(0.99)}
  100% {transform: scale(1.0)}

}

@media screen and (max-width: 850px){
  .title_1 {
  font-size: 20px;
  }
  .image {
  width: 80vw;
}

}
</style>