<template>
  <div class="footer_container">
    <footer class="py-3 my-4">
      <ul class="nav justify-content-center pb-3 mb-3">
        <li class="nav-item"><a @click="ChangePageMain" class="nav_link nav-link px-2 text-muted">Gówny</a></li>
        <li class="nav-item"><a @click="ChangePageMusic" class="nav_link nav-link px-2 text-muted">Muzyka</a></li>
        <li class="nav-item"><a @click="ChangePageGreen" class="nav_link nav-link px-2 text-muted">Survival Zielony</a></li>
        <li class="nav-item"><a @click="ChangePageMilitary" class="nav_link2 nav-link px-2 text-muted">Survival Militarny</a></li>
        <li class="nav-item"><a @click="ChangePageCity" class="nav_link3 nav-link px-2 text-muted">Survival Miejski</a></li>
        <div v-if="info" style="background: linear-gradient(to left, darkred, white);" class="line"></div>
        <div v-else-if="info2" style="background: linear-gradient(to left, blue, white);" class="line"></div>
        <div v-else class="line"></div>

      </ul>
      <a href="https://github.com/WladykaPawel" class="signature text-center text-muted">© 2022 WladykaPawel</a>
    </footer>
  </div>
</template>

<script>
export default {
  name: "FooterLine",
  props:{
   info: Boolean,
   info2: Boolean
  },
  methods:
  {
    ChangePageMain()
    {
      this.$emit('first', this.main)
    },
    ChangePageMusic()
    {
      this.$emit('second', this.music)
    },
    ChangePageGreen()
    {
      this.$emit('third', this.green)
    },
    ChangePageMilitary()
    {
      this.$emit('fourth', this.military)
    },
    ChangePageCity()
    {
      this.$emit('fifth', this.city)
    }

  }
}
</script>

<style scoped>
.footer_container
{
  width: 100vw;
  background: none;
  margin-bottom: -50px;
  margin-top: -200px;
  z-index: 1;
}
.nav_link
{
  color: white!important;
  font-weight: 600;
  font-size: 20px;
  text-shadow: 0 0 0.2em #000, 0 0 0.2em #000, 0 0 0.2em #000;
}
.nav_link2
{
  color: white!important;
  font-weight: 600;
  font-size: 20px;
  text-shadow: 0 0 0.2em #000, 0 0 0.2em #000, 0 0 0.2em #000;
}
.nav_link3
{
  color: white!important;
  font-weight: 600;
  font-size: 20px;
  text-shadow: 0 0 0.2em #000, 0 0 0.2em #000, 0 0 0.2em #000;
}

.nav-item
{
  padding-left: 15px;
  padding-right: 15px;
}
.text-center
{
  color: white!important;
  font-weight: 600;
  text-shadow: 0 0 0.2em #000, 0 0 0.2em #000, 0 0 0.2em #000;
}
.nav_link:hover
{
  cursor: pointer;
  color: #24801a!important;
}
.nav_link2:hover
{
  cursor: pointer;
  color: darkred!important;
}
.nav_link3:hover
{
  cursor: pointer;
  color: blue!important;
}
.line
{
  width: 80vw;
  height: 2px;
  background: linear-gradient(to left, green, white);
  margin-top: 20px;
}
.signature
{
  text-decoration: none;
}
.signature:hover
{
  text-decoration: underline;
}
@media screen and (max-width: 850px){
  .footer_container {
  margin-top: -325px;
  }

}
</style>