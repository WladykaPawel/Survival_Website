<template>
  <div class="component_container">
    &emsp; &emsp; Wybierając się na dłuższą wyprawę bardzo ważnym elementem survivalu jest wybranie odpowiedzniego miejsca do spania, oraz przygotowania go poprawnie
    biorąc pod uwagę warunki pogodowe oraz bezpieczeństwo.
  </div>
  <div class="main">
    Rodzaje schronień na noc lub złą pogodę podczas survivalu można podzielić na 3 kategorie:
  </div>
    <div class="button_container">
      <button class="button_page"  @click="selected_kind='naturalne'">Nauralnie utworzone </button>
      <button class="button_page"  @click="selected_kind='przygotowane'">Wcześniej przygotowane </button>
      <button class="button_page"  @click="selected_kind='wykonane'">Samodzielnie wykonane </button>
    </div>

  <div v-if="selected_kind=='naturalne'" class="kinds">
      Nauralnie utworzone
    <ul>
      <li class="list">
        <div class="title">Jaskinia</div>
          Najbardziej bezpieczny i komfortowy wybór podczas nocy. W Polsce ze względu na nizinne ukształtowanie terenu nie ma dużej liczby jaskiń. W Tatrach Zachodnich jest ich około 700, w Górach Świętokrzyskich około 200, w Pieninach niecałe 50, natomiast w Karpatach około 800.
          Planując wyprawę, warto dokładnie zapoznać się z pokonywanym terenem, może akurat uda się zlokalizować przyjemne miejsce na nocleg.
          Jaskinia daje schronienie, które swobodnie można dopasować do swoich indywidualnych potrzeb.
          Pierwszym elementem adaptacji jest rozpalenie ogniska w odpowiednim miejscu. Dzięki dobrej osłonie istnieje duża szansa, że jaskinia zatrzyma wysoką temperaturę i stworzy przyjemne miejsce do spania.
          Drugim krokiem jest zabezpieczenie wejścia. Po pierwszym sprawdzeniu może wydawać się, że jaskinia nie jest zamieszkała przez jakieś zwierzę, jednak z czasem może się okazać, że lokator wyszedł tylko na polowanie. Wejście do jaskini warto zablokować gałęziami, które powinny na noc odstraszyć zwierzynę.
          Przed rozłożeniem posłania należy także dobrze zaizolować podłoże. Dzięki temu będzie można przespać noc w komfortowych warunkach.
      </li>
      <li class="list">
        <div class="title">Zagłębienie w skale</div>
        Niestety nie na każdej trasie wyprawy survivalowej można znaleźć wygodną i przestronną jaskinię do przeczekania nocy. Zagłębienie w skale nie jest najbardziej komfortowym miejscem do noclegu, ale może się okazać jedynym rozwiązaniem na trasie.
        W tym wypadku do stworzenia bazy warto wykorzystać folię NRC, która ochroni przed wiatrem i pozwoli zachować stałą temperaturę.
        W zagłębieniu może być trudno przyjąć pozycję leżącą, dlatego warto przygotować się na wymagającą noc. Jeśli jednak kolejnego dnia zawodnik planuje powrót do wspinaczki czy wymagającej górskiej wyprawy, powinien poszukać bardziej wygodnego miejsca, które pozwoli na w miarę spokojny odpoczynek.
      </li>
      <li class="list">
        <div class="title">Gęstwina</div>
        Nie zawsze istnieje szansa na odkrycie jakiegokolwiek miejsca, w którym można się schować, a w wyposażeniu survivalowca mogło nie być miejsca na namiot. W takim wypadku warto skorzystać z naturalnej ochrony, jaką dają gęste korony drzew.
        Latem noce w lasach nie są aż tak chłodne, by nie móc spać pod gołym niebem. Temperaturę pomoże także utrzymać rozpalone ognisko. Gęste drzewa chronią przed wiatrem, a także możliwymi opadami deszczu.
        Oprócz ogniska można odizolować podłoże i zabezpieczyć gałęziami pobliski teren. Dzięki temu zmniejsza się ryzyko pojawienia się dzikiej zwierzyny.
        Duża powierzchnia i miękkie podłoże umożliwiają rozłożenie legowiska i wyspanie się w komfortowych warunkach, porównywalnych do tych, które można stworzyć w przytulnej jaskini.
      </li>
      <li class="list">
        <div class="title">Zwalone Drzewo</div>
        Konar obalonego drzewa na pierwszy rzut oka może nie stanowić dobrej ochrony. Tego typu lokalizacja musi zostać odpowiednio przygotowana i zmodyfikowana na potrzeby noclegu.
        Powalone drzewo jest jednym z najczęściej występujących elementów krajobrazu leśnego, dlatego znalezienie odpowiedniego nie powinno być tak trudne, jak na przykład poszukiwanie jaskini. Przed rozpoczęciem budowy odpowiedniego schronienia należy dokładnie sprawdzić, czy gałęzie i inne elementy drzewa są stabilne i nie grożą zawaleniem pod wpływem silniejszego powiewu wiatru.
        Warto także sprawdzić kierunek wiatru, tak aby ulokować się po przeciwnej stronie drzewa.
        Niedaleko obalonego konara można rozpalić ognisko i przygotować całą bazę. Podobnie jak w przypadku spania w gęstwinie, warto zabezpieczyć teren gałęziami i zaizolować podłoże. Jeśli drzewo znajduje się w obniżeniu terenu to należy pamiętać, że temperatura w zagłębieniu będzie niższa.
        Oprócz wykorzystania folii NRC można zabezpieczyć podłoże grubą warstwą liści czy ściółki, a sam konar otoczyć zabudowanymi ścianami szałasu.
      </li>

    </ul>
  </div>
  <div v-else-if="selected_kind=='przygotowane'" class="kinds">
    Wcześniej przygotowane
    <ul>
      <li class="list">
          <div class="float">
            <img class="image" src="@/assets/Green_survival/namiot.jpg" alt="namiot">
            <div>
              <div class="title">Namiot</div>
              Namiot to chyba pierwsza rzecz jaką ma się na myśli słysząc "biwak". Ważne jest by był wodoodporny, oraz lekki (w szczegolności dla osób którzy podróżują pieszo)
              Warto zaopatrzeć się w namiot mający tzw. tropik z przedsionkiem, to pozwala nam lepiej zagospodarować miejsce podczas dłuższego pobytu.
            </div>

          </div>
      </li>
      <li class="list">
          <div class="float">
             <img class="image" src="@/assets/Green_survival/śpiwór.png" alt="spiwor">
            <div>
              <div class="title">Śpiwór</div>
              Podczas pierwszych wypadów, dobry i ciepóły śpirór to podstawa. W nocy nawet w lecie temperatura bardzo mocno spada, więc ogrzanie się w śpiworze jest bardzo ważne
            </div>
          </div>
      </li>
      <li class="list">
          <div class="float">
            <img class="image" src="@/assets/Green_survival/hamak.jpg" alt="hamak">
            <div>
              <div class="title">Hamak</div>
              Jest to stosunkowo nowy sposób spania w dziczy, lecz bardzo wygodny, w przeciweństwie do namiotu hamak jest bardzo lekki.
              Spanie whamaku zapewnia także bezpieczeństwo ze strony małych stworzeń czy owadów które podczas spania na ziemi mogą być uciążliwe
            </div>
          </div>
      </li>
      <li class="list">
           <div class="float">
             <img class="image" src="@/assets/Green_survival/auto.jpg" alt="auto">
             <div>
               <div class="title">Spanie w aucie</div>
               Chociaż brzmi to niedorzecznie spanie w aucie może byc całkiem wygodne, a na rynku jest mnóstwo dmuchanych materacy zapewniających komfort podczas tego wyboru.
               Spanie w aucie jest też stosunkowo bezpieczne, bo można się zamknąć od środka i zabezpieczyc przed poencjalnym niebezpieczeńswem
             </div>
           </div>
      </li>

    </ul>
  </div>
  <div v-else-if="selected_kind=='wykonane'" class="kinds">
    Samodzielnie wykonane
    <div class="self">
      Przygotowywanie sobie własnego miejsca do spania jest ciężkie i uzależnione od sytuacji klimatycznej. W niektorych obszarach świata są to igla lub lodowe jamy, w innych chatki z gliny lub liści palm
      W Polsce jednak najcześciej buduje się schronienia z gałęzi i innych rzeczy znalezionych w lesie, ze względu na łatwą dostępnośc materiałów. Mimo tego istnieje wiele rodzajów schronień,
      mające swoje plusy i minusy.
    </div>
    Tu będzie kontynuacja...
    <br>
    <br>

  </div>
</template>

<script>
export default {
  name: "PlaceToSleepPage",
  data(){
    return{
      selected_kind:'naturalne',
      kinds:[
        {kind:'naturalne'}  ,
        {kind:'przygotowane'},
        {kind:'wykonane'}
      ]

    }
  }

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
  padding: 30px 15vw 30px 15vw;
  color: #4c4c4c;
  font-size: 25px;
  text-align: justify;
}
.button_container
{
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 20px 0 20px 0;
}
.button_page
{
  padding: 15px;
  margin: 10px 20px 10px 20px;
  width: 240px;
  font-size: 24px;
  text-align: center;
  cursor: pointer;
  outline: none;
  color: #fff;
  background-color: green;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}
.button_page:hover
{
  background-color: darkgreen;
}
.button_page:active {
  background-color: darkgreen;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
.button_page:focus {
  background-color: limegreen;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
.kinds
{
  width: 70vw;
  border-radius: 10px;
  margin: 20px;
  color: #4c4c4c;
  padding-top: 20px;
}
.list
{
  font-size: 20px;
  text-align: justify;
  list-style: none;
  padding: 20px 50px 20px 20px;
  margin-top: 50px;
   background: #FFFFFF;
  border-radius: 20px;
}
.title
{
  color: #24801a;
  font-size: 30px;
  padding: 10px;
}
.image
{
  padding: 20px;
  width: 30vw;
  height: 20vw;
  border-radius: 45px;
  opacity: 1;
  transition: 1.5s;
  float: left;
  /*shape-outside: ellipse(100px 235px at 68% 26%);*/
}

.image:hover
{
 opacity: 0.7;
 cursor: pointer;
}
.float
{
  min-height: 20vw ;
}
.self
{
  font-size: 20px;
  text-align: justify;
  list-style: none;
  padding: 20px 50px 20px 20px
}

@media screen and (max-width: 850px){
  .button_container
  {
    flex-direction: column;
  }
  .button_page
  {
    width: 70vw;
  }
  .image{
    width: 60vw;
    height: 40vw;
    padding-left: 0;
  }
  .list
  {
    font-size: 15px;
    text-align: justify;
    list-style: none;
  }

}

</style>