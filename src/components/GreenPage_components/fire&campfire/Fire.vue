<template>
  <div class="title">
    Rozpalanie Ognia
    <div class="title_desc">
      Lubując się w wypadach survivalowych, warto znać kilka niezawodnych sposobów na rozpalenie ogniska.
      Sprawdź, co ze sobą zabrać i jak zaprószyć ogień bez pomocy zapałek czy zapalniczki!
    </div>
  </div>
  <ul class="description">
      <li class="items">
        <h1 class="title_1">Sposób 1: Rozpalanie łukiem ogniowym</h1>
        <div class="fire_container">
          <img class="fire_image" src="../../../assets/Green_survival/fire_styles/łuk_ogniowy.jpg" alt="łuk ogniowy">
          <div class="fire_descriprion">
            Ogień rozpalisz również łukiem ogniowym. Jest to jednak czasochłonna i pracochłonna metoda, tradycyjna i mniej praktyczna w porównaniu do współczesnych sposobów.
            Niemniej warto wiedzieć, w jaki sposób zbudować i jak wykorzystać łuk ogniowy. Odsyłam Was do <a href="https://youtu.be/P73VoLN2yS4" target="_blank">filmu Bushcraftowego</a>
        </div>
        </div>
      </li>
      <li class="items">
        <h1 class="title_1">Sposób 2: Rozpalanie lupą</h1>
        <div class="fire_container">
          <img class="fire_image" src="../../../assets/Green_survival/fire_styles/lupa.jpg" alt="lupa">
          <div class="fire_descriprion">
            W celu rozpalenia ognia najpierw należy wytworzyć żar przez skupienie promieni słońca na hubce. Po około minucie pojawiają się smużki dymu a hubka zaczyna się tlić.
            Przesuwając zogniskowane promienie po powierzchni hubki staramy się uzyskać żar na jej większej powierzchni. Ułatwi to i przyspieszy rozpalenie podpałki.
            Kiedy hubka już tli się na powierzchni ok pół cm kwadratowego możemy zakończyć rozpalanie jej lupą. Teraz hubkę należy włożyć na rozpałce z drobnej trawy i mchu i rozpocząć rozdmuchiwanie żaru.
          </div>
        </div>
      </li>
      <li class="items">
        <h1 class="title_1">Sposób 3: Rozpalanie krzesiwem magnezowym</h1>
        <div class="fire_container">
          <img class="fire_image" src="../../../assets/Green_survival/fire_styles/krzesiwo_magnezowe.jpg" alt="krzesiwo">
          <div class="fire_descriprion">
            Rozpalanie wykonuje się przez energiczne potarcie blaszką lub nożem po pręcie krzesiwa nad zgromadzoną rozpałką. Rozpałka powinna być drobna i sucha.
            Jeżeli takiej nie ma to dobrze jest dodać do niej kawałek hubki lub zwęglonej bawełny,
            które przechwycą iskry i zaczną się tlić. Potem wystarczy rozdmuchać żar tak by spowodował on zapłon podpałki. Gotowe!
          </div>
        </div>
      </li>
      <li class="items">
        <h1 class="title_1">Sposób 4: Rozpalanie rolowaniem</h1>
        <div class="fire_container">
          <img class="fire_image" src="../../../assets/Green_survival/fire_styles/rolowanie.jpg" alt="rolowanie">
          <div class="fire_descriprion">
            Najpierw należy stwozyć tzw. kokon. W tym celu można wykorzystać szmatkę, włókna lub płatki bawełniane. Na bawełnę nakładamy popiół i zwijamy tworząc „kokon”.<br>
            Rozpalanie wykonuje się przez energiczne „wałkowanie” dociskiem wykonanego „kokona”. Po około minucie rolowania bierzemy „kokon” i sprawdzamy czy jego temperatura wzrasta. Jeżeli nic się nie dzieje należy ponowić wałkowanie.
            Zdumiewające jest wrażenie kiedy po wykonaniu „wałkowania kokona” czuć w dłoni wzrastającą temperaturę w jego wnętrzu. W pewnym momencie zaczyna parzyć. Pojawia się żar i dym.
          </div>
        </div>
      </li>
  </ul>
</template>

<script>
export default {
  name: "FirePage"
}
</script>

<style scoped>
.title{
  margin: 20px 0 10px 0;
}

.title_desc
{
  color: #4c4c4c;
  font-size: 18px;
  text-align:  justify;
  margin: 20px 12vw 50px 12vw;
}
.description
{

  color: #4c4c4c;
  font-size: 20px;
  text-align: justify;
  padding: 0 10vw 10px 10vw;
}
.title_1
{
  color: #24801a;
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
  padding: 0 5vw 50px 5vw;
}
.fire_container
{
  display: flex;
  justify-content: space-between;
}
.fire_descriprion
{
  padding: 10px 10px 10px 30px;
}
.fire_image
{
  margin-left: 50px;
  width: 20vw;
  height: 12vw;
  border-radius: 20px;
}

.fire_image:hover
{
 opacity: 0.9;
}

@media screen and (max-width: 1400px){
  .fire_container
{
  display: flex;
  flex-direction: column;
    align-items: center;
  justify-content: space-between;
}

  .fire_descriprion
{
  padding: 10px 10px 10px 10px;
}
.fire_image
{
  margin-left: 0;
  width: 40vw;
  height: 24vw;
}

}
</style>