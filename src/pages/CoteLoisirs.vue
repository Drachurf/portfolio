<template>
  <h4> Le sport </h4>
  <p>Je pratique le sport depuis l'âge de 4 ans. J'ai commencé par le rugby, que j'ai pratiqué pendant une vingtaine d'années. J'ai également pratiqué le basketball, un sport dans lequel j'ai connu le haut niveau, jouant pour les équipes départementales puis régionales de mon secteur. J'ai même réussi à décrocher le titre de champion de France lors de mes années minimes.</p>
  <p>Depuis, je continue à pratiquer le sport, mais je suis surtout un bénévole engagé auprès des associations dans lesquelles je suis actif. Lorsque je jouais au rugby à Pessac, j'étais trésorier de mon association. Actuellement basketteur à Biscarrosse, je suis responsable de la partie partenariats du club.</p>
  <h4> Les voyages </h4>
  <div class="boxmap">
  <div id="l-container"></div>
  </div>
  <p class="legende"> A chaque marqueur une image de l'un de mes voyages </p>
</template>

<script>
import "leaflet/dist/leaflet.css";
import L from 'leaflet';

import imgNewYork from "../assets/images/marker/newyork.webp";
import imgMongolie from "../assets/images/marker/mongolie.webp";
import imgMoscou from "../assets/images/marker/moscou.webp";
import imgRoumanie from "../assets/images/marker/roumanie.webp";
import imgLondres from "../assets/images/marker/londres.webp";
import imgBarca from "../assets/images/marker/barca.webp";
import imgCork from "../assets/images/marker/cork.webp";
import imgYogya from "../assets/images/marker/yogi.webp";
import imgBromo from "../assets/images/marker/bromo.webp";
import imgMalaisie from "../assets/images/marker/malaisie.webp";
import imgItalie from "../assets/images/marker/sardainge.webp";
import imgCroatie from "../assets/images/marker/croatie.webp";
import imgLisbonne from "../assets/images/marker/lisbonne.webp"
import imgStPet from "../assets/images/marker/stpet.webp";
import imgCardiff from "../assets/images/marker/cardiff.webp";
import imgStEul from '../assets/images/marker/steEule.webp';
import imgAthenes from '../assets/images/marker/Athenes.webp';
import logoMarker from '../assets/logo/location-dot-solid.svg';


export default {
  name: "LeafletMapView",
  data() {
    return {
      center: [44.0875, -1.1989],
      lmap: null,
      zoom: 3
    };
  },
  methods: {
    /**
     * Init Leaflet map
     * 
     * @param {number[]} mapcenter center of the map in EPSG:3857
     * @param {number} mapzoom zommlevel
     * @returns {Map} initmap new leaflet map
     */
    setupLeafletMap(mapcenter, mapzoom) {
      let initmap = L.map("l-container").setView(mapcenter, mapzoom);
      L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
        maxZoom: 5,
        minZoom: 2.8,
        attribution: '&copy; Openstreetmap France | &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
      }).addTo(initmap);
      return initmap;
    },

    /**
     * Add markers to the map
     */
     addMarkers() {
  const cities = [
    { name: "New York", location: [40.7128, -74.0060], image: imgNewYork },
    { name: "Oulan-Bator", location: [47.9188, 106.9170], image: imgMongolie },
    { name: "Moscou", location: [55.7558, 37.6176], image: imgMoscou },
    { name: "Roumanie", location: [45.9432, 24.9668], image: imgRoumanie },
    { name: "Londres", location: [51.5099, -0.1180], image: imgLondres },
    { name: "Barcelone", location: [41.3851, 2.1734], image: imgBarca },
    { name: "Cork", location: [51.8974, -8.4728], image: imgCork },
    { name: "Yogyakarta", location: [-7.7971, 110.3686], image: imgYogya },
    { name: "Bromo", location: [-7.9425, 112.9531], image: imgBromo },
    { name: "Malaisie", location: [4.2105, 101.9758], image: imgMalaisie },
    { name: "Italie", location: [41.9028, 12.4964], image: imgItalie },
    { name: "Croatie", location: [45.1000, 15.2000], image: imgCroatie },
    { name: "Lisbonne", location: [38.7223, -9.1393], image: imgLisbonne },
    { name: "Saint-Pétersbourg", location: [59.9343, 30.3351], image: imgStPet },
    { name: "Cardiff", location: [51.4816, -3.1791], image: imgCardiff },
    { name: "Sainte Eulalie En Born", location: [44.308019,  -1.181046], image: imgStEul },
    {name: "Athenes", location: [37.9838, 23.7275], image: imgAthenes}
  ];

  const defaultIcon = L.icon({
    iconUrl: logoMarker,
    iconSize: [30, 30],
    iconAnchor: [15, 30],
    popupAnchor: [0, -30],
  });

  cities.forEach(city => {
    const marker = L.marker(city.location, { icon: defaultIcon }).addTo(this.lmap);

    // Personnalisez la popup avec le nom de la ville et une image
    const popupContent = `
      <div style="display: flex; flex-direction: column; text-align: center;">
        <p>${city.name}</p>
        <img src="${city.image}" alt="${city.name}" style="width: 100px; height: auto;">
      </div>
    `

    marker.bindPopup(popupContent);
  });
},
  },
  mounted() {
    this.lmap = this.setupLeafletMap(this.center, this.zoom);
    this.addMarkers();
  },
};
</script>

<style scoped>
#l-container {
  height: 500px;
  width: 90%;
}
.legende{
font-style: italic;
font-size: medium;
}
.boxmap{
  width: 100%;
  display: flex;
  justify-content: center;
}
@media screen and (max-width: 767px) {
  #l-container {
  height: 500px;
  width: 80%;
}
}
</style>
