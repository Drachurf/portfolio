<template>
  <div class="flexAround">
    <div class="boxGauche">
      <h3>Expériences Professionnelles</h3>
      <h4 @click="toggleExp('Larrere')" :class="{ 'active': activeExp === 'Larrere' }">2023 - 2024 Developpeur web <br>Les
        Fermes Larrere</h4>
      <h4 @click="toggleExp('MTC')" :class="{ 'active': activeExp === 'MTC' }">2018 - 2022 Praticien Traditionnelle
        Chinois <br> Praticien libéral</h4>
      <h4 @click="toggleExp('APF')" :class="{ 'active': activeExp === 'APF' }">2017 - 2020 Educateur Spécialisé <br> APF
        France Handicap</h4>
      <h4 @click="toggleExp('T21')" :class="{ 'active': activeExp === 'T21' }">2015 - 2017 Educateur Spécialisé <br>
        Trisomie 21 </h4>
    </div>
    <div class="boxDroite">
      <h3>Détail de l'expérience</h3>
      <div v-if="activeExp === 'Intro'" class="expContent, warning">
        <p><strong>
          Cliquez sur les expériences sur votre gauche pour avoir plus de détails.
        </strong></p>
      </div>
      <div v-if="activeExp === 'Larrere'" class="expContent Larrere">
        <p>Aux Fermes larres depuis aout 2023, Mes objectifs sont de répondre aux besoins des professionnels de
          l’entreprise. Ainsi les différents professionnels peuvent me solliciter pour mettre en place des applications
          permettant de soulager leur quotidien.
          En tant qu'alternant développeur web au sein des Fermes, mon rôle principal est de concevoir, développer et
          maintenir des applications web répondant aux besoins spécifiques des professionnels. Je travaille en étroite
          collaboration avec les différentes équipes pour comprendre leurs exigences et traduire ces besoins en solutions
          logicielles efficaces. Mon objectif est de contribuer au renforcement des capacités digitales de l'entreprise en
          créant des applications intuitives et fonctionnelles.
        </p>
      </div>
      <div v-if="activeExp === 'MTC'" class="expContent MTC">
        <p>Durant 4 années, j'ai été auto-entrepreneur, dans l'accompagnement au bien-être pour les clients venant me
          voir. Après avoir aidé des individus dans le cadre social de mon métier d'éducateur spécialisé, j'ai souhaité
          accompagner des personnes différemment dans une approche holistique. Projet qui m'a beaucoup plu durant ces 4
          années avec une autonomie importante du fait que j'étais mon propre patron.</p>
      </div>


      <div v-if="activeExp === 'APF'" class="expContent APF">
        <p>Expérience à mi-temps durant laquelle j'ai monté des projets pour des personnes en situation de handicap. Le
          SAVS (Service d'Accueil à la Vie Sociale), propose des accompagnements pour des personnes majeures avec un
          handicap moteur. Durant ces 3 ans j'ai travaillé en équipe pluriprofessionnelle dans la construction du projet
          de service et la mise en place d'une charte qualité.",</p>
      </div>


      <div v-if="activeExp === 'T21'" class="expContent T21">
        <p>Expérience de deux ans pour l'association Trisomie 21. Mon but était d'accompagner des personnes porteur de
          trisomie 21 dans leur projet d'autonomie. Durant ces deux années j'ai été formé au Facile à Lire et à Comprendre
          (FALC) permettant de mettre en forme des documents pour l'adapter aux handicaps (de façon générale). <strong>Je peux donc réaliser
          des sites web adaptés au besoin de personnes en situation de handicap.</strong>

        </p>
      </div>

    </div>
  </div>
</template>
  
<script>


export default {
  data() {
    return {
      activeExp: 'Intro'
    };
  },
  methods: {
    toggleExp(exp) {
      this.activeExp = (this.activeExp === exp) ? null : exp;
    }
  }
};
</script>

  
<style>
.active {
  text-decoration: none;
  background-color: rgba(210, 105, 30, 0.721);
  color: black;
  margin: 1%;
  padding: 2%;
  border-radius: 10px;
}
.warning{
  border: 1px solid black;
  padding: 1%;
  border-radius: 10px;
  text-align: center;
}
.expContent {
  text-align: justify;
}
@media screen and (max-width: 767px){
  .flexAround{
    font-size: medium;
  }
}
</style>
  