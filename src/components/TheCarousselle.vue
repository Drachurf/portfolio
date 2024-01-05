<template>
    <div class="boxCarousel">
      <h2>Mes réalisations : </h2>
      <Carousel :itemsToShow="1" :wrapAround="true" :transition="500">
        <Slide class="flexColumn" v-for="slide in slides" :key="slide.id">
          <img class="carousel__item" :src="slide.imageSrc" alt="Slide {{ slide.id }}" />
          <legend class="flexColumn"> {{ slide.legendImage }} 
            <a v-if="slide.link" :href="slide.link">Cliquez ici pour accéder au site en ligne</a>
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
import image2 from '../assets/images/sitesWeb/wallstreet/wsf1.webp';
import image3 from '../assets/images/sitesWeb/OCR/p2.webp';
import image4 from '../assets/images/sitesWeb/OCR/p5.webp';
import image5 from '../assets/images/sitesWeb/OCR/p6.webp';
import image6 from '../assets/images/sitesWeb/OCR/p7.webp';


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
        { id: 1, imageSrc: image1, legendImage: "AppTract' : Application permettant de calculer le cout d'une machine agricole." },
        { id: 2, imageSrc: image2, legendImage: "Wall Street Farm : Application permettant de créer des produits, apports, en vu de gérer les stocks d'aliments en direct pour les ventes commerciales." },
        { id: 3, imageSrc: image3, 
          legendImage: "Bookie : exercice OpenClassRooms, reproduire en Html et Css un design depuis une maquette figma.", 
          link: 'https://drachurf.github.io/p2/',},
        { id: 4, imageSrc: image4, legendImage: "Portfolio de Nina Carducci : exercice OpenClassRooms. Optimisation SEO d'un site web.", 
          link: 'https://drachurf.github.io/p5/', },
        { id: 5, imageSrc: image5, legendImage: "Kasa : exercice OpenClassRooms. A partir du maquette figma, reproduire un site web en React",
          link: 'https://drachurf.github.io/p6/', },
        { id: 6, imageSrc: image6, legendImage: "Mon vieux grimoire : exercice OpenClassRooms. Réalisation d'un backend avec Nodejs et Mongodb",
           },
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
  min-height: 200px;
  width: 70%;
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

</style>