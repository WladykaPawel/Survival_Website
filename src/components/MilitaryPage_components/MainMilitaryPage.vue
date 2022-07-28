<template>
    <div class="description w3-animate-top">

      <img class="image" src="@/assets/Military_survival/topsecret.png">

    </div>
</template>

<script>
export default {
  name: "MainMilitarypage",

}
</script>


<style scoped>

.description
{
  color: darkred;
}

.image
{
  width: 40vw;
}
.image:hover
{
  animation: shake 1s infinite linear;
}

@keyframes shake{
  25% {
    transform: scale(1.01);
  }
  75% {
    transform: scale(0.99);

  }
  100% {
    transform: scale(1.0)
  }
}


</style>