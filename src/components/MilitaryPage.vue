<template>
  <div class="container_military">
    <div class="title">
      Survival Militarny
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
}
.title
{
  color: darkred;
  padding: 30px 10px;
  font-family: fantasy;
  letter-spacing: 2px;
}

</style>