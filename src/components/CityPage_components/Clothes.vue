<template>
  <div class="Clothes_desc">
    ODZIEŻ
    <div class="Clothes_main">
      <ul class="description">
        <img class="image" src="@/assets/City_survival/odziez.jpg" alt="odzież">
        <li class="items">
          <h1 class="title_1">Bielizna</h1>
          Mam tu na myśli skarpety i gatki. Ze zrozumiałych względów (higienicznych) potrzebujesz przynajmniej dwóch kompletów.
          Szczególną uwagę zwróć na skarpety. Zadbaj, by były grube (wolniej się zużywają) i nie obcierały.
          Dobrym wyborem będzie tu wełna. Jest ciepła i grzeje nawet, gdy jest mokra. Takie skarpety przydadzą się nawet latem.
        </li>
        <li class="items">
          <h1 class="title_1">Bielizna termiczna</h1>
          Nieodzowny element survivalowej odzieży. Standardowy układ to „kalesonki” i koszulka z długim rękawem wykonane z
          łatwo odprowadzających pot, szybkoschnących i elastycznych materiałów. Latem chłodzą, zimą grzeją.
        </li>
        <li class="items">
          <h1 class="title_1">Buty</h1>
          Rzecz absolutnie kluczowa. Muszą być wygodne i mocne. Powinny mieć grubą i przyczepną podeszwę oraz usztywniać kostki.
          Wspinając się na gruzowiska albo biegając w kółko po schodach (windy przecież nie działają) łatwo o kontuzję. Solidnie je też zaimpregnuj.
        </li>
        <li class="items">
          <h1 class="title_1">Spodnie</h1>
          Ważne, by były wytrzymałe i funkcjonalne. Dobrym wyborem są modele przeznaczone dla wojska.
          Mają zazwyczaj sporo ergonomicznie ułożonych kieszeni, szyte są z mocnych i „trudnopalnych” materiałów.
          Wybierając jakieś, musisz jednak zwrócić uwagę na pokrywający je kamuflaż. Niektóre jego typy (np. pustynne),
          zamiast wtapiać Cię w szarość i brud miasta, mogą ściągać niepotrzebne spojrzenia.
        </li>
        <li class="items">
          <h1 class="title_1">Bluza</h1>
          Możesz ją traktować bądź jako zewnętrzną warstwę „funkcjonalną”, która pozwoli Ci poupychać po kieszeniach różne graty,
          bądź jako kolejną warstwę grzewczą. W pierwszym wariancie dobrym wyborem będą różnej maści bluzy wojskowe, w drugim polary lub softshelle.
        </li>
        <li class="items">
          <h1 class="title_1">Kurtka przeciwdeszczowa lub ponczo</h1>
          Tu wszystko jest jasne. Jak pada, wyciągasz kurtkę z plecaka i zakładasz na grzbiet.
        </li>
        <li class="items">
          <h1 class="title_1">Nakrycie głowy</h1>
          Tu mamy do wyboru klasyczną czapkę „bejsbolówkę”, „panamę”, chustę, szalokominiarkę itd. Dwie ostanie chronią przed pyłem. Czapka z daszkiem osłania oczy przed słońcem. Dla każdego coś miłego.
        </li>
        <li class="items">
          <h1 class="title_1">Rękawiczki</h1>
          Po raz kolejny sprawa jest jasna. Chronią przed chłodem i otarciami. Jeśli zawierają np. kevlar, to w jakimś stopniu chronią też przed przecięciami, a więc i przed ostrzem noża.
        </li>
    </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "ClothesPage"
}
</script>

<style scoped>
.Clothes_desc
{
  color: blue;
  padding: 50px 20px 20px 20px;
}
.Clothes_main
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

</style>