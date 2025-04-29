<template>
  <div class="boxformation">
    <details open>
      <summary >2024 - 2026 - Data Analyst - OpenClassRoom</summary>
      <p>
        Formation en alternance au sein de la Direction de l'Audit Interne de la caisse d'épargne Aquitaine Poitou Charente.
        objectif de foramtion : <br>
        - Réaliser des modélisations de données pour segmenter une audience marketing.<br>
        - Analyser les ventes en vue d'améliorer la stratégie de l'entreprise. <br>
        - Interroger une base de données statistiques pour répondre à des questions business.<br>
        - Réaliser des dashboards avec graphiques et indicateurs de suivi pour suivre et analyser des résultats.<br>
        - Collecter, agréger et nettoyer des données en vue de réaliser une étude de marché. <br>
        Technologies : Python, Jupiter, MySQL, PostgreSQL, SQL, Knime, PowerBI, Pandas, Numpy, Matplotlib, Seaborn.
      </p>
    </details>

    <details>
      <summary>2023 - 2024 - Bachelor du numérique - Campus Landes</summary>
      <p>
        Formation en alternance avec les Fermes Larrere <br>
        Objectif de formation : <br>
        - Maîtriser les technologies web modernes (JavaScript, React, Node.js, PHP, etc.) <br>
        - Développer des applications sécurisées et performantes <br>
        - Intégrer des solutions cloud et DevOps <br>
        Travailler en mode projet Agile / Scrum <br>
      </p>
    </details>

    <details>
      <summary>Décembre 2022 - Mai 2023 - Développeur Web - OpenClassRoom</summary>
      <div>
        Objectif de formation : <br>
        - Construire un site web responsive et dynamique s’adaptant à tout type d’écran grâce à l’intégration des éléments des maquettes graphiques (développement front-end avec HTML, CSS, JavaScript et React) <br>
        - Créer des API et des bases de données pour développer des sites complets et dynamiques et assurer le bon fonctionnement côté serveur (développement back-end avec NodeJS, Express et MongoDB). <br>
        - Optimiser les performances et réaliser la maintenance de sites web déjà existants pour permettre leur fonctionnement optimal et une bonne visibilité sur les moteurs de recherche (SEO). <br>
        - Gérer un projet web de A à Z : de la planification du projet à la présentation de la solution au client, en passant par la rédaction des spécifications techniques. <br>
        Technologies : HTML, CSS, JavaScript, React, Git/GitHub, NodeJS, Express, MongoDB, les API REST
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
        spécialisédès la sortie de ma formation.
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
  background-color: #e1a23f;
  border: 1px solid #ccc;
  border-radius: 10px;
}

details>div {
  padding: 0.5em;
  border-top: none;
  border-radius: 0 0 10px 10px;
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
  