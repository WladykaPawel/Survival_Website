<template>
  <div class="component_container">
    <div class="main">
      &emsp; &emsp; W każdym lesie, mogą czyhać na Ciebie różne niebezpieczeństwa. Nie tylko ze strony zwierząt, ale też pogody, czy… niewiedzy, dlatego
      przygotowanie to jedna z najważnejszych rzeczy w survivalu. Należy być przygotowanym zarówno teorytycznie jak praktycznie. Przygotowanie praktyczne jest to także
      wyposażenie się w wszelkiego rodzaju akcesoria, bardzo przydające się w trudnych sytuacjach, a także nieraz niezbędnych do przetrwania.
    </div>
    <ul class="description">
      <li class="items">
        <h1 class="title_1">Zadbaj o odpowiednie jedzenie</h1>
        Wyprawa do lasu nie jest możliwa bez odpowiedniego przygotowania logistycznego.
        Mimo tego że wiele rzeczy do jedzenia jesteś w stanie zdobyć samemu w lesie, to (w szczególności w początkowej fazie "zabawy" z survivalem) warto zaopatrzyć się w jedzenie.
        Najlepiej sycące, zajmujące mało miejsca i kaloryczne.
        Doskonałym pomysłem na jedzenie "w dziczy" są różnego rodzaju konserwy, przede wszystkim te wojskowe lub całe zestawy zawane "Racjami żywnościowymi".
        <img class="image" src="@/assets/Green_survival/racje.jpg">
        <i class="image_descriprion">Przykładowa racja żywnościowa</i>
        <br>
        Oprócz tego warto zabierać produkty liofilizowane.
        <br>
        <br>
        Ważnym elementam są także napoje. Najlepiej brać ze sobą czytą wodę, lub urządzenie zdolne udatnić płynącą lub stojącą wodę do spożycia. Warto też zabrać ze sobą parę torebek herbarty,
        kawy lub innych napojów w proszku, aby urozmaicić sobie je podczas wyprawy .
      </li>
      <li class="items">
        <h1 class="title_1">Dobry nóż to podstawa</h1>
        Bez noża praktycznie nie mamy czego szukać w lesie. Stawiając na model myśliwski,
        warto wybrać najbardziej uniwersalny i niezawodny w sytuacjach kryzysowych model.
      </li>
      <li class="items">
        <h1 class="title_1">Latarka – by rozproszyć ciemność</h1>
        Przejście niektórych etapów szlaku w nocy wymaga odpowiedniego oświetlenia. Wówczas najlepiej sprawdzają się latarki czołowe.
        Oprócz latarki warto wziąć ze sobą druga mniejszą która będzie służyła nam awaryjnie, a także zapasowe baterie. Można też zakupić
        latarkę którą można ładować, m.in. dzięki słońcu lub sile naszych dłoni.
        <br>
        Przydatne jest kiedy latarka na którą się decydujemy ma parę trybów świecenia.
      </li>
      <li class="items">
        <h1 class="title_1">Krzesz ogień!</h1>
        Dobrze przygotowane ognisko pozwala się ogrzać, ale też przygotować część posiłków. Nie zawsze jednak potrzebne są zapałki, których zastosowaine ogranicza wilgoć.
        Zapalniczka na benzynę jest dobrym wyborem, lecz niezawodnym sposobem do rozpalenia ognia jest krzesiwo magnesowe, lub zapalacz.
        <img class="image" src="@/assets/Green_survival/Krzesiwo.png">
        <i class="image_descriprion">Krzesiwo magnezowe</i>
      </li>
      <li class="items">
        <h1 class="title_1">Wskazówka, by się nie zgubić</h1>
        Kompas to absolutnie jeden z najważniejszych elementów wyposażenia podczas survivalu. Możesz wybrać prostą busolę –
        z muszką i szczerbinką, lub też bardziej zaawansowany model z linijką ułatwiający naniesienie przebiegu trasy na mapę.
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "PreparationPage"
}
</script>

<style scoped>

.component_container
{

}
.main
{
  padding: 30px;
  color: #4c4c4c;
  font-size: 20px;
  text-align: justify;
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
.image
{
  width: 30vw;
  align-items: center;
  padding: 30px 30px 10px 30px ;
  transition: 1s;
}
.image:hover
{
  cursor: pointer;
}
.image_descriprion
{
  font-size: 15px;
}
</style>