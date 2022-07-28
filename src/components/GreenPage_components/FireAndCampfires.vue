<template>
    <div>
      <button class="button_page"  @click="selected_theme='ogien'">Rozpalanie Ognia </button>
      <button class="button_page"  @click="selected_theme='ogniska'">Rodzaje Ognisk </button>
    </div>
    <div v-if="selected_theme=='ogien'">
      <FirePage></FirePage>
    </div>
    <div v-else-if="selected_theme=='ogniska'">
      <CampfirePage></CampfirePage>
    </div>
</template>

<script>
import FirePage from "@/components/GreenPage_components/fire&campfire/Fire";
import CampfirePage from "@/components/GreenPage_components/fire&campfire/Campfire";
export default {
  name: "FireAndCampfiresPage",
  components: {CampfirePage, FirePage},
  data() {
    return{
      selected_theme:'ogien',
      themes:[
        {theme:'ogien'},
        {theme:'ogniska'}
      ]
    }
  }
}
</script>

<style scoped>

.button_page
{
  padding: 15px 25px;
  margin: 10px 20px 10px 20px;
  width: 250px;
  font-size: 24px;
  text-align: center;
  cursor: pointer;
  outline: none;
  color: #fff;
  background-color: green;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}
.button_page:hover
{
  background-color: darkgreen;
}
.button_page:active {
  background-color: darkgreen;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}
.button_page:focus {
  background-color: limegreen;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}

</style>