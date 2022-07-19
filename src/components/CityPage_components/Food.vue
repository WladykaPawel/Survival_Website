<template>
  <div class="Food_desc">
    ŻYWNOŚĆ
    <div class="Food_main">
      <ul class="description">
        <img class="image" src="@/assets/City_survival/zywnosc.jpg" alt="żywność">
        <li class="items">
          <h1 class="title_1">Manierka lub bidon</h1>
          Jednym słowem, pojemnik na wodę. Najlepiej z filtrem.
        </li>
        <li class="items">
          <h1 class="title_1">Filtr do wody</h1>
           Jak coś się poważnie posypie, to woda przestanie płynąć z kranów. To masz jak w banku. A pić musisz. Dlatego urządzenie, które pomoże Ci uzdatnić znalezioną wodę jest arcyistotne.
        </li>
        <li class="items">
          <h1 class="title_1">Kuchenka i zapas paliwa</h1>
          Może być nawet malutki Esbit. Ciepłe żarcie to naprawdę ważna sprawa.
        </li>
        <li class="items">
          <h1 class="title_1">Żelazna racja</h1>
          Na dno plecaka wsadź kilka konserw, liofilizaty albo wysokoenergetyczne jedzenie z szalup ratunkowych. Zjesz je dopiero, gdy zaczniesz się zastanawiać, czy zbrojony beton lepiej smakuje kiszony, czy marynowany.
        </li>
        <li class="items">
          <h1 class="title_1">„Kondensaty kaloryczne”</h1>
          Mówiąc wprost, słodkości. Dobrze jest mieć gdzieś w zanadrzu np. czekoladę – krzepi i podnosi morale.
        </li>
        <li class="items">
          <h1 class="title_1">Niezbędnik i menażka</h1>
          Czymś i na czymś jeść przecież musisz. Im lżejsze, tym lepsze.
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "FoodPage"
}
</script>

<style scoped>
.Food_desc
{
  color: blue;
  padding: 50px 20px 20px 20px;
}
.Food_main
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