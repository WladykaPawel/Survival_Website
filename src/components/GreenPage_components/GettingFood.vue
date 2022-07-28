<template>
  <div class="component_container">
    <div class="main">
      &emsp; &emsp; Koczowanie w dziczy wymaga odpowiedniego przygotowania. Jedną z kilku kluczowych kwestii, na które należy zwrócić szczególną uwagę, jest żywność.
      Jakie jedzenie najlepiej sprawdzi się podczas wyprawy survivalowej?
    </div>
    <ul class="description">
      <li class="items">
        <h1 class="title_1">Rośliny</h1>
        Większość ziół , jakie znamy i używamy w domu mogą być naszym pożywieniem. Jadalna jest mięta pieprzowa ( ta od dolegliwości żołądkowych) ,
        można żuć także jej świeże liście. Jadalny jest dziurawiec (drobne żółte kwiatki i dziurki w liściach). Jadalny jest szczaw, mlecz (mniszek lekarski), koniczyna.
        Wiosną gdy liście są świeże i jeszcze nie takie twarde ( nie zawierają jeszcze zbyt dużo celulozy ) nadają się do jedzenia np. liście Buka.

      </li>
      <li class="items">
        <h1 class="title_1">Sok z drzew</h1>
        Wiosenny sok z Brzozy zawiera duże ilości węglowodanów.
        Aby go pozyskać należy wywiercić mały otwór w gałęzi lub pniu drzewa, i gdy zacznie wyciekać sok można go zebrać w jakieś naczynie.<br>
        Można też koniec uciętej gałęzi wsadzić do butelki i czekać aż sok napełni butelkę.
      </li>
      <li class="items">
        <h1 class="title_1">Żywność z drzew</h1>
          Oprócz oczywistego pożywienia takim jakie są owoce drzew (jabłka, gruszki, śliwki, itp...) oraz orzechy, które dzięki dużej zawartości tłuszczu są bardzo pożywne,
          dzięki drzewom możemy zdobyć także inne pożywienie.<br>
          Dużo węglowodanów znajduje się w szyszkach roślin iglastych. Aby je wydobyć należy szyszki rozdrobnić i
          mieszać w wodzie o temperaturze około 40 ° C przez około 20 minut.
          Jadalna jest również kora po wewnętrznej stronie młodych brzóz i sosen. I to zarówno gotowana jak i na surowo.
      </li>
      <li class="items">
        <h1 class="title_1">Wodorosty</h1>
          Można bez obaw spożywać morskie wodorosty oraz rośliny słodkowodne i ich kłącza (np. bulwy tataraku) Obie te grupy są bardzo pożywne.
      </li>
      <li class="items">
        <h1 class="title_1">Grzyby</h1>
          Wybierając grzyby jako swoje pożywnienie, należy wybierać tylko te którch gatunków jesteśmy pewni. Wiele trujących grzybów może nam przynieść więcej szkody niż pożytku.
      </li>
    </ul>
    <div id="Warning">
      UWAGA! Szukając pożywnienia należy uważać na trujace Rośliny, Owoce i Grzyby!
    </div>
  </div>
</template>

<script>
export default {
  name: "GettingFoodPage"
}
</script>

<style scoped>
.component_container
{
  padding: 30px;
  color: #4c4c4c;
  font-size: 20px;
  text-align: justify;
  scroll-behavior: smooth;
}
.main
{
  margin-bottom: 50px;
}
.description
{

  color: #4c4c4c;
  font-size: 20px;
  text-align: justify;
  padding: 0 10vw 10px 10vw;
}
.title_1
{
  color: #24801a;
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
}
#Warning
{
  text-align: center;
  font-size: 40px;
  animation: shake 1s infinite linear;
  font-family: fantasy;
}

@keyframes shake{
  25% {
    transform: scale(1.01);
    color: #9b3d3c;
  }
  75% {
    transform: scale(0.99);

  }
  100% {
    transform: scale(1.0)
  }
}

@media screen and (max-width: 850px){
.description
{
  padding: 0 1vw 10px 1vw;
  font-size: 16px;
}
.title_1
{
  font-size: 25px;
}
.items
{
  padding: 0 10vw 50px 10vw;
}
#Warning
{
  font-size: 20px;
}


}


</style>