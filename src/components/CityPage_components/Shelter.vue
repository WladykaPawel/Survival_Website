<template>
  <div class="Shelter_desc">
    SCHRONIENIE
    <div class="Shelter_main">
      <ul class="description">
        <img class="image" src="@/assets/City_survival/schronienie.jpg" alt="schronienie">
        <li class="items">
          <h1 class="title_1">Śpiwór</h1>
          Najlepiej lekki i ciepły. Za taki jednak sporo zapłacisz.
        </li>
        <li class="items">
          <h1 class="title_1">Karimata</h1>
          Możesz też sięgnąć po wojskową, na przykład z holenderskiego demobilu. Albo po tzw. samopompę. Trzeba jednak uważać, by nie przebił jej szklany odłamek lub wystający pręt.
        </li>
        <li class="items">
          <h1 class="title_1">Brezent z oczkami i ekspandery lub płachta biwakowa</h1>
           Po pierwsze chroni przed wiatrem, deszczem lub śniegiem. Po drugie sprawia, że po rozpaleniu ognia możesz ją odpowiednio zawiesić i uniknąć „wścibskich” spojrzeń. Po trzecie można nią zasłonić okna, drzwi itp.
        </li>
      </ul>

    </div>
  </div>
</template>

<script>
export default {
  name: "ShelterPage"
}
</script>

<style scoped>
.Shelter_desc
{
  color: blue;
  padding: 50px 20px 20px 20px;
}
.Shelter_main
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