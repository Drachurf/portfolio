<template>    

<h3>Loisirs</h3>
  <ul>
      <li>Rugby : 20 ans de pratique 🏉</li>
      <li>Basket-ball : Niveau national 🏀</li>
  </ul>
  <hr>
  <h3>Les voyages</h3>
  <div class="map">
    <l-map ref="map" v-model:zoom="zoom" :center="[47.41322, -1.219482]">
      <l-tile-layer
        url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
        layer-type="base"
        name="OpenStreetMap">
      </l-tile-layer>
      <l-marker v-for="(position, index) in markerPositions" :key="index" :lat-lng="position" @click="onMarkerClick">
        <l-popup>
          <div>
            <h4>{{ getCityName(index) }}</h4>
            <img :src="getCityImage(index)" alt="City Image" style="max-width: 100%; height: auto;">
          </div>
        </l-popup>
      </l-marker>
    </l-map>
  </div>
</template>

<script>
import "leaflet/dist/leaflet.css";
import { LMap, LTileLayer, LMarker, LPopup } from "@vue-leaflet/vue-leaflet";

export default {
  components: {
    LMap,
    LTileLayer,
    LMarker,
    LPopup,
  },
  data() {
    return {
      zoom: 2,
      markerPositions: [
        [40.7128, -74.0060],  // New York
        [47.9188, 106.9170],  // Oulan-Bator
        [55.7558, 37.6176],   // Moscou
        [45.9432, 24.9668],   // Roumanie
        [51.5099, -0.1180],   // Londres
        [41.3851, 2.1734],    // Barcelone
        [51.8974, -8.4728],   // Cork
        [-7.7971, 110.3686],  // Yogyakarta
        [-7.9425, 112.9531],  // Bromo
        [4.2105, 101.9758],   // Malaisie
        [41.9028, 12.4964],   // Italie
        [45.1000, 15.2000],   // Croatie
        [38.7223, -9.1393],   // Lisbonne
        [59.9343, 30.3351],   // Saint-Pétersbourg
        [51.4816, -3.1791],   // Cardiff
      ],
      cityImages: [
        require('@/assets/images/marker/mongolie-Petite.webp'),// New York CHANGER
        require('@/assets/images/marker/mongolie-Petite.webp'),  // Oulan-Bator
        require('@/assets/images/marker/morcow-Petite.webp'), // Moscou
        require('@/assets/images/marker/reouaie-Petite.webp'), // Roumanie
        require('@/assets/images/marker/mongolie-Petite.webp'), // Londres CHANGER
        require('@/assets/images/marker/barca - Petite.webp'),  // Barcelone
        require('@/assets/images/marker/cork - Petite.webp'), // Cork
        require('@/assets/images/marker/yogi.webp'), // Yogyakarta
        require('@/assets/images/marker/bromo.webp'), // Bromo
        require('@/assets/images/marker/malaisie-Petite.webp'), // Malaisie
        require('@/assets/images/marker/sardainge-Petite.webp'), // Italie
        require('@/assets/images/marker/croatie1 - Petite.webp'), // Croatie
        require('@/assets/images/marker/lisbonne-Petite.webp'), // Lisbonne
        require('@/assets/images/marker/st-Petite.webp'), // Saint-Pétersbourg
        require('@/assets/images/marker/cardiff.webp'), // Cardiff
      ],
    };
  },
  methods: {
    onMarkerClick() {
      // Ne fait rien ici, la popup s'ouvre automatiquement avec le contenu
    },
    getCityName(index) {
      // Retournez le nom de la ville en fonction de l'index
      const cityNames = [
        'New York', 'Oulan-Bator', 'Moscou', 'Roumanie', 'Londres',
        'Barcelone', 'Cork', 'Yogyakarta', 'Bromo', 'Malaisie',
        'Italie', 'Croatie', 'Lisbonne', 'Saint-Pétersbourg', 'Cardiff'
      ];
      return cityNames[index];
    },
    getCityImage(index) {
      // Retournez l'URL de l'image de la ville en fonction de l'index
      return this.cityImages[index];
    },
  },
};
</script>
<style>
hr{
  border: 2px solid black;
}
.map{
  height:500px
}
@media screen and (max-width: 767px){
  .map{
    margin: 0px 5%

  }
}
  </style>