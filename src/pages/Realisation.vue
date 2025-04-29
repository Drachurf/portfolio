<template>
    <div class="boxCarousel">
      <Carousel :itemsToShow="1" :wrapAround="true" :transition="500">
        <Slide class="flexColumn" v-for="slide in slides" :key="slide.id">
          <img class="carousel__item" :src="slide.imageSrc" alt="Slide {{ slide.id }}" />
          <legend class="flexColumn"> {{ slide.legendImage }} 
            <a v-if="slide.link" :href="slide.link" target="_blank">Cliquez ici pour avoir plus de détails sur la réalisation</a>
          </legend>  
        </Slide>
        
        <template #addons>
          <Navigation />
          <Pagination />
        </template>
      </Carousel>
    </div>
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Navigation, Pagination } from 'vue3-carousel';

import image1 from '../assets/images/sitesWeb/apptract/apptract1.webp';
import image1_1 from '../assets/images/sitesWeb/apptract/apptract5.webp';
import image2 from '../assets/images/sitesWeb/wallstreet/wsf1.webp';
import image3 from '../assets/images/sitesWeb/OCR/p2.webp';
import image4 from '../assets/images/sitesWeb/OCR/p5.webp';
import image5 from '../assets/images/sitesWeb/OCR/p6.webp';
import image6 from '../assets/images/sitesWeb/OCR/p7.webp';
import image7 from '../assets/images/sitesWeb/OCR/Datanalyste/p8.webp';
import image8 from '../assets/images/sitesWeb/OCR/Datanalyste/p9.webp';
import image9 from '../assets/images/sitesWeb/OCR/Datanalyste/p10.webp';
import image10 from '../assets/images/sitesWeb/OCR/Datanalyste/p11.webp';
//import image11 from '../assets/images/sitesWeb/OCR/Datanalyste/p12.webp';



export default {
  components: {
    Carousel,
    Slide,
    Navigation,
    Pagination,
  },
  data() {
    return {
      selectedImage: null,
      slides: [
        { id: 1, imageSrc: image1, legendImage: "AppTract : Application permettant de calculer le coût d'une machine agricole." },
        { id: 2, imageSrc: image1_1, legendImage: "AppTract : Application permettant de calculer le coût d'une machine agricole." },
        { id: 3, imageSrc: image2, legendImage: "Wall Street Farm : Application permettant de créer des produits, apports, en vue de gérer les stocks d'aliments en direct pour les ventes commerciales." },
        { id: 4, imageSrc: image3, legendImage: "Bookie : exercice OpenClassRooms, reproduire en Html et Css un design depuis une maquette figma.", link: 'https://github.com/Drachurf/Dev_P2',},
        { id: 5, imageSrc: image4, legendImage: "Portfolio de Nina Carducci : exercice OpenClassRooms. Optimisation SEO d'un site web.", link: 'https://github.com/Drachurf/Dev_P5', },
        { id: 6, imageSrc: image5, legendImage: "Kasa : exercice OpenClassRooms. A partir d'une maquette figma, reproduire un site web en React", link: 'https://github.com/Drachurf/Dev_P6',},
        { id: 7, imageSrc: image6, legendImage: "Mon vieux grimoire : exercice OpenClassRooms. Réalisation d'un backend avec Nodejs et Mongodb", link: 'https://github.com/Drachurf/Dev_P7',},
        { id: 8, imageSrc: image7, legendImage: "Analyse des indicateur de l'égalité hommes/femmes", link: 'https://github.com/Drachurf/DA_P8', },
        { id: 9, imageSrc: image8, legendImage: "Analyse des ventes d'une librairie", link: 'https://github.com/Drachurf/DA_P9',},
        { id: 10, imageSrc: image9, legendImage: "Projet libre : analyse à partir de données sur la NBA" , link: 'https://github.com/Drachurf/DA_P10',},
        { id: 11, imageSrc: image10, legendImage: "Produire une étude de marché", link: 'https://github.com/Drachurf/DA_P11',},
        //{ id: 12, imageSrc: image11, legendImage: "Détecter des faux biellets", link: 'https://github.com/Drachurf/DA_P12',},
      ],
    };
  },
};
</script>
<style scoped>
.flexColumn{
  display: flex;
  flex-direction: column;
}
.carousel__item {
  height: 500px;
  width: 60%;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 2%;
}
legend{
  cursor: pointer;
}
a{
  text-decoration: none;
  color : rgba(210, 105, 30, 0.721) ;
}
@media screen and (max-width: 767px){
 .carousel__item{
  height: 150px;
 }
}
</style>