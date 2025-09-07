<template>
      <h3>Cliquez sur une expérience à gauche pour plus de détail</h3>
      <hr>
      <div class="thebox">
  <div class="flexAround">
    <div class="boxGauche">
      <h4 @click="toggleExp('CEAPC')" :class="{ 'active': activeExp === 'CEAPC' }">2024 - 2025 Data Analyst <br>DAI Caisse d'Epargne</h4>
      <h4 @click="toggleExp('Larrere')" :class="{ 'active': activeExp === 'Larrere' }">2023 - 2024 Developpeur web <br>Les
        Fermes Larrere</h4>
      <h4 @click="toggleExp('MTC')" :class="{ 'active': activeExp === 'MTC' }">2018 - 2022 Praticien Traditionnel
        Chinois <br> Praticien libéral</h4>
      <h4 @click="toggleExp('APF')" :class="{ 'active': activeExp === 'APF' }">2017 - 2020 Educateur Spécialisé <br> APF
        France Handicap</h4>
      <h4 @click="toggleExp('T21')" :class="{ 'active': activeExp === 'T21' }">2015 - 2017 Educateur Spécialisé <br>
        Trisomie 21 </h4>
    </div>
    <div class="boxDroite">
      <h3>Détail de l'expérience</h3>
      <div v-if="activeExp === 'Intro'" class="expContent, warning">
      </div>
      <div v-if="activeExp === 'CEAPC'" class="expContent CEAPC">
        <p> Au sein du service de la direction de l'audit interne, mon objectif est d'aider les collaborateurs de la Caisse d'Épargne dans leurs missions d'audit. Ainsi, ils font des demandes de données, et j'ai pour mission de récupérer ces données, de les nettoyer et de les transformer pour les rendre lisibles et exploitables.
            J'ai réalisé une mini-application alimentée automatiquement par un séquenceur Alteryx dans le but d'assurer une actualisation des données de façon mensuelle ou semestrielle. Cette automatisation permet de gagner un temps précieux et de réduire les erreurs humaines.
            J'ai également réalisé un travail de nettoyage des données pour élaborer une cartographie RH et financière des différentes agences du territoire. Ce travail a permis d'améliorer la visibilité et la prise de décision stratégique en facilitant l'accès à des informations fiables et à jour.
        </p>
      </div>
      <div v-if="activeExp === 'Larrere'" class="expContent Larrere">
        <p>Mes objectifs étaient de répondre aux besoins des professionnels de l’entreprise. Ainsi, les différents professionnels pouvaient me solliciter pour mettre en place des applications permettant de soulager leur quotidien.
            En tant qu'alternant développeur web au sein des Fermes, mon rôle principal était de concevoir, développer et maintenir des applications web répondant aux besoins spécifiques des professionnels. Je travaillais en étroite collaboration avec les différentes équipes pour comprendre leurs exigences et traduire ces besoins en solutions logicielles efficaces. Mon objectif était de contribuer au renforcement des capacités digitales de l'entreprise en créant des applications intuitives et fonctionnelles.
            J'ai notamment créé une application métier permettant aux commerciaux de l'entreprise d'avoir des données de vente en temps réel.</p>
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
          (FALC) permettant de mettre en forme des documents pour l'adapter aux handicaps (de façon générale).

        </p>
      </div>

    </div>
  </div>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      activeExp: 'CEAPC'
    };
  },
  methods: {
    toggleExp(exp) {
      this.activeExp = (this.activeExp === exp) ? null : exp;
    }
  }
};
</script>

  
<style scoped>
.thebox{
    display: flex;
    justify-content: center;
}
.flexAround{
  display: flex;
  justify-content: space-around;
  width: 80%;
}
.boxGauche{
  width: 30%;
}
.boxDroite{
  width: 60%;
}
h3{
  margin-top: 20px;
  width: 100%;
  text-align: center;
  margin-bottom: 25px;
}
.active {
  text-decoration: none;
  background-color: #e1a23f;
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
h4{
cursor: pointer;
}
@media screen and (max-width: 767px){
  .flexAround{
    font-size: medium;
  }
}
</style>
  