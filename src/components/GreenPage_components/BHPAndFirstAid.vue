<template>
  <div class="descriptionBHP">
    Chwila nieuwagi, źle zrobiony krok i patrzysz bezradnie jak twój towarzysz wędrówki przewraca się i doznaje kontuzji.
    Podczas gdy w obszarze gęsto zaludnionym pomoc nadciąga w ciągu kilku minut, o tyle w plenerze jesteś pierwszą osobą, która będzie zobowiązana do niesienia pomocy.
    Dowiesz się tutaj, jak się zachować w sytuacjach awaryjnych i jak zdobyć większą pewność siebie biorąc udział w kursach z udzielania pierwszej pomocy w terenie.
  </div>
    <div class="main">
      <div class="points">
        <b> 1. Zachowaj spokój</b><br>
        Jeśli dotrzesz na miejsce wypadku jako pierwszy, pamiętaj o najważniejszej zasadzie: zachować spokój.
        W ten sposób możesz skuteczniej nadzorować sytuację i skuteczniej udzielać pierwszej pomocy.
        Ratownik, który emanuje spokojem, daje również poczucie bezpieczeństwa poszkodowanemu.<br>
      </div>
      <div class="points">


      <b>2. Oceń niebezpieczeństwo</b><br>
      Szybko rozeznaj sytuację: Czy teren jest niebezpieczny? Czy istnieje np. dalsze ryzyko osuwania się kamieni?
      W sytuacjach awaryjnych, w których zagrożone jest twoje bezpieczeństwo, w pierwszej kolejności ratuj swoje życie.
      Wybierz numer alarmowy i nie narażaj się na żadne niebezpieczeństwo.<br>
      </div>
      <div class="points">


      <b>3. Zabezpiecz miejsce wypadku</b><br>
      Jeśli poszkodowany znajduje się w obszarze niebezpiecznym (np. na ruchliwej drodze lub na górskim szlaku rowerowym tuż za zakrętem),
      musisz zabezpieczyć miejsce wypadku (np. skrzyżowanymi kijkami trekkingowymi przed zakrętem).<br>
      </div>
      <div class="points">


      <b>4. Co stało się z osobą poszkodowaną?</b><br>
      Jeśli poszkodowany jest nieprzytomny, ma silne krwawienie lub skarży się na ból w klatce piersiowej,
      nie wolno tracić czasu. W tych zagrażających życiu sytuacjach kryzysowych liczy się każda sekunda.<br>
      </div>
      <div class="points">


      <b>5. Zadzwoń pod numer alarmowy</b><br>
      Już w wielu wypadkach telefon komórkowy uratował życie. Dlatego zawsze noś go przy sobie.
      Jeśli znasz krajowy numery alarmowe ratownictwa górskiego, wybierz ten numer.
      W polskich górach to numery do GOPR (Górskie Ochotnicze Pogotowie Ratunkowe): 985 lub 601 100 300. Numer ratunkowy nad wodą to: 601 100 100.
      Pod numerem alarmowym 112 możesz uzyskać pomoc w całej Europie. Uwaga: jeśli wybierasz się poza Europę, zdecydowanie powinieneś zapisać numer telefonu alarmowego.<br>
      </div>
      <div class="points">

      <b>6. Dzwoniąc pod numer alarmowy odpowiedz na pięć pytań:</b><br>
      Kto dzwoni?<br>
      Gdzie zdarzył się wypadek?<br>
      Co się stało?<br>
      Ilu jest poszkodowanych?<br>
      Odpowiedz na zadane pytania<br>
      Bardzo ważna dla służb ratowniczych jest przede wszystkim dokładna lokalizacja miejsca wypadku.
      Idealnym rozwiązaniem jest jeśli masz pod ręką dane GPS lub mapę turystyczną,
      W przeciwnym razie podaj charakterystyczne punkty orientacyjne (np. polana, ostatnie skrzyżowanie).
      Następnie zawsze trzymaj swój telefon komórkowy w pobliżu, aby być dostępnym w razie jakichkolwiek dalszych pytań.
      </div>

    </div>
</template>

<script>
export default {
  name: "BHPAndFirstAidPage"
}
</script>

<style scoped>

.descriptionBHP
{
  font-size: 22px;
  color: green;
  text-align: justify;
  text-transform: uppercase;
  margin: 0 8vw 0 8vw;
}

.descriptionBHP:hover
{
  color: darkgreen;
}

.points
{
  background-color: white;
  margin-top: 20px;
  padding: 20px;
  border-radius: 20px;
}
.points:hover
{
  background: linear-gradient(to left, white, limegreen);
}


.main
{
  font-size: 18px;
  color: #4c4c4c;
  margin: 50px 10vw 10px 10vw;
  text-align: justify;
}
@media screen and (max-width: 850px){
  .descriptionBHP
  {
    font-size: 16px;
    margin: 0 6vw 0 6vw;
  }
  .main
  {
    font-size: 14px;
    margin: 30px 8vw 10px 8vw;
  }

}


</style>