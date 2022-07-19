<template>
  <div class="container_city">
    <div class="title">
    Survival Miejski
    </div>
  </div>
</template>

<script>
export default {
  name: "CityPage"
}
</script>

<style scoped>
.container_city
{
  background-size: cover;
  background-image: linear-gradient(rgba(255,255,255,0.5), rgba(255,255,255,0.5)), url("../assets/city_survival.jpg");
  min-height: 1000px;
  margin-bottom: -10px;
}
.title
{
  color: blue;
  padding: 30px 10px;
  font-family: fantasy;
  letter-spacing: 2px;
}

</style>