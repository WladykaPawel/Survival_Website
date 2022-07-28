<template>
  <div class="container_military">
    <div class="title w3-animate-right">
      Survival Militarny
    </div>
    <div class="main_military w3-animate-left">
        Chwilowy brak zawartości :)<br>
    </div>
    <video class="movie"  width="500" height="300" controls>
      <source src="../assets/movie.mp4" type="video/mp4">
    </video>

    <MainMilitarypage> </MainMilitarypage>
  </div>
</template>

<script>
import MainMilitarypage from "@/components/MilitaryPage_components/MainMilitaryPage";
export default {
  name: "MilitaryPage",
  components: {MainMilitarypage}
}
</script>

<style scoped>
.container_military
{
  background-size: cover;
  background-image: linear-gradient(rgba(255,255,255,0.5), rgba(255,255,255,0.5)), url("../assets/military_survival.jpg");
  min-height: 1000px;
  margin-bottom: -10px;
  padding-bottom: 200px;
}
.title
{
  color: darkred;
  padding: 30px 10px;
  font-family: fantasy;
  letter-spacing: 2px;
}
.main_military
{
  margin: 20px;
  font-size: 30px;
  color: black;
}
.movie{
  margin:200px 0 -400px 0;
}

</style>