<template>
  <h3>Formations :</h3>
  <div class="boxformation">
    <details>
      <summary>2023 - 2024 - Bachelor du numérique - Campus Landes</summary>
      <p>
        Formation en alternance avec les Fermes Larrere, objectif :
        être capable d’analyser les besoins et de proposer des solutions
        adaptées dans le domaine de la conception et de la gestion de systèmes d’information. De plus, la méthode de
        gestion de projet, la capacité à communiquer, prendre des initiatives et des responsabilités seront des notions
        qui seront approfondies. Option : développeur.
      </p>
    </details>

    <details>
      <summary>Décembre 2022 - Mai 2023 - Développeur Web Bac +2 - OpenClassRoom</summary>
      <div>
        Formation de développer web sur 6 mois. Vous trouverez mes projets en dessous 👇. Voici les technologies
        apprises durant la formation : HTML - CSS - JavaScript - React - MongoDB - NodeJS. La formation propose
        également
        un
        projet de gestion de projet où j’ai pu appréhender la méthode Agile. Enfin, il y a un projet d’optimisation où
        il
        faut rendre un site accessible, avec des performances optimisées et un bon référencement SEO.
      </div>
    </details>

    <details>
      <summary> 2015 - 2020 Praticien en médecine traditionnelle chinoise - IFTEM</summary>
      <div>
        La formation proposée par l'IFTEM (Institut de Formation aux Thérapies Energétiques et Manuelles) est disposée sur
        les te mps de weekend. J'ai donc, pendant 5 ans, associé la formation de cette école avec le métier d'éducateur
        spécialisé. J'ai obtenu le diplôme de praticien en médecine chinoise après ces 5 ans de formation.
      </div>
    </details>

    <details>
      <summary>2012 - 2015 Diplôme d'Etat d'Educateur Spécialisé - IRTS </summary>
      <div>
        Diplôme d'Etat d'Educateur Spécialisé (bac +3), formation de 3 ans durant laquelle j'ai effectué 4 stages, 3
        de trois mois et un d'un an. Formation validée avec succès qui m'a permis d'exercer le métier d'éducateur
        spécialisé
        dès la sortie de ma formation.
      </div>
    </details>


    <details>
      <summary> 2008 - 2010 Science Technologie Sanitaire et Sociale Bac - Lycée les Bourdonnières - Nantes</summary>
      <div>
        Diplôme de niveau bac technologique, domaine Science Technologique Sanitaire et Sociale.
      </div>
    </details>
  </div>
</template>  
  
<script>
</script>
  
<style scoped>
.boxformation {
  display: flex;
  flex-direction: column;
  align-items: center;

}

details {
  text-align: justify;
  margin-bottom: 10px;
  width: 90%;
}

summary {
  cursor: pointer;
  outline: none;
  user-select: none;
  padding: 0.5em;
  font-weight: bold;
  background-color: rgba(210, 105, 30, 0.721);
  border: 1px solid #ccc;
  border-radius: 10px;
}

details>div {
  padding: 0.5em;
  border-top: none;
  border-radius: 0 0 10px 10px;
  background-color: #CBD7E4;
}
@media screen and (max-width: 767px){
  .boxformation{
    font-size: medium;
  }
  summary{
    font-size: large;
  }
}
</style>
  