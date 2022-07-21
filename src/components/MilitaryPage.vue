<template>
  <div class="container_military">
    <div class="title w3-animate-right">
      Survival Militarny
    </div>
    <div class="main_military w3-animate-left">
        Chwilowy brak zawartości :)
    </div>
  </div>
</template>

<script>
export default {
  name: "MilitaryPage"

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

</style>