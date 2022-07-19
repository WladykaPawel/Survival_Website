<template>
  <div class="Electronic_desc">
    ELEKTRONIKA
    <div class="Electronic_main">
      <ul class="description">
        <img class="image" src="@/assets/City_survival/Elektronika.jpg" alt="elektronika">
        <li class="items">
          <h1 class="title_1">Telefon i ładowarka</h1>
          Rzecz bardzo ważna. Jak działa GPS i Internet, a Ty masz dostęp do prądu, to możesz nawigować i komunikować się ze światem. Gorzej, jak to wszystko wysiądzie.
          Zawsze jednak zostanie Ci pobrana wcześniej mapa okolicy. I latarka.
        </li>
        <li class="items">
          <h1 class="title_1">Powerbank</h1>
           Wiadoma sprawa. Kilkanaście godzin pracy telefonu ekstra.
        </li>
        <li class="items">
          <h1 class="title_1">Przenośny panel fotowoltaiczny</h1>
          Pozwoli naładować telefon. O ile świeci słońce.
        </li>
        <li class="items">
          <h1 class="title_1">Kable USB</h1>
          Może się przydadzą? Kto wie?
        </li>
        <li class="items">
          <h1 class="title_1">Latarka i zapas baterii</h1>
          Kolejna oczywistość. Najczęściej wybierana jest czołówka. Sprawia, że masz wolne ręce. Możesz się czegoś chwycić, coś trzymać albo komuś przypieprzyć.
        </li>
      </ul>

    </div>
  </div>
</template>

<script>
export default {
  name: "ElectronicPage"
}
</script>

<style scoped>
.Electronic_desc
{
  color: blue;
  padding: 50px 20px 20px 20px;
}
.Electronic_main
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