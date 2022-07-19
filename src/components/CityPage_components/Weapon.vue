<template>
  <div class="Weapon_desc">
    BROŃ
    <div class="Weapon_main">
      <ul class="description">
        <img class="image" src="@/assets/City_survival/bron.jpg" alt="broń">
        <li class="items">
          <h1 class="title_1">Palna</h1>
          Kolejna oczywista oczywistość. W sytuacji kryzysowej czasem nie ma po prostu innego wyjścia, trzeba strzelać. Kompaktowy, łatwy do ukrycia i niezwodny Glock 19 wydaje się być optymalnym wyborem. Nie zapomnij o kilku zapasowych magazynkach na podorędziu.
        </li>
        <li class="items">
          <h1 class="title_1">Biała</h1>
           Zamiast morgenszternów, buzdyganów i nadziaków sugeruję, byś zaopatrzył się w łatwy do ukrycia i przenoszenia składany nóż. Nim przynajmniej obierzesz ziemniaki.
        </li>
        <li class="items">
          <h1 class="title_1">Miotająca</h1>
          Czyli łuk, kusza lub proca. Tu się nie ma co śmiać. Strzały, bełty i pociski są ciche, a po wystrzeleniu czasem można je odzyskać. W ostateczności da się je wytworzyć metodami chałupniczymi. A „amunicja” do procy często leży wprost na ulicy.
        </li>
        <li class="items">
          <h1 class="title_1">Gaz Pieprzowy</h1>
          Czasem agresora wystarczy po prosu zdezorientować. Odrobina żelu ze stężoną kapsaicyną dobrze się do tego nadaje.
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "WeaponPage"
}
</script>

<style scoped>
.Weapon_desc
{
  color: blue;
  padding: 50px 20px 20px 20px;
}
.Weapon_main
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