<template>
  <div class="boxnav">
    <nav>
      <a href="#" :class="{ active: currentComponent === 'CoteProfessionnel' }"
        @click.prevent="showComponent('CoteProfessionnel')"> Expériences professionnelles</a>
      <a href="#" :class="{ active: currentComponent === 'CoteEtudiant' }"
        @click.prevent="showComponent('CoteEtudiant')">Formations</a>
      <a href="#" :class="{ active: currentComponent === 'Realisation' }"
        @click.prevent="showComponent('Realisation')">Mes réalisations</a>
      <a href="#" :class="{ active: currentComponent === 'SoftKills' }" @click.prevent="showComponent('SoftKills')">Soft
        Kills</a>
      <a href="#" :class="{ active: currentComponent === 'CoteLoisirs' }"
        @click.prevent="showComponent('CoteLoisirs')">Loisirs</a>

    </nav>
  </div>
  <CoteProfessionnel v-if="currentComponent === 'CoteProfessionnel'" />
  <CoteEtudiant v-if="currentComponent === 'CoteEtudiant'" />
  <CoteLoisirs v-if="currentComponent === 'CoteLoisirs'" />
  <Realisation v-if="currentComponent === 'Realisation'" />
  <SoftKills v-if="currentComponent === 'SoftKills'" />
</template>

<script>
import CoteEtudiant from '../pages/CoteEtudiant.vue';
import CoteLoisirs from '../pages/CoteLoisirs.vue';
import CoteProfessionnel from '../pages/CoteProfessionnel.vue';
import Realisation from '../pages/Realisation.vue';
import SoftKills from '../pages/SoftKills.vue';

export default {
  data() {
    return {
      currentComponent: 'CoteProfessionnel',
    };
  },
  mounted() {
    const savedComponent = sessionStorage.getItem('currentComponent');
    if (savedComponent) {
      this.currentComponent = savedComponent;
    }
  },
  methods: {
    showComponent(componentName) {
      if (this.currentComponent === componentName) {
        this.currentComponent = null;
        sessionStorage.removeItem('currentComponent');
      } else {
        this.currentComponent = componentName;
        sessionStorage.setItem('currentComponent', componentName);
      }
    },
  },
  components: {
    CoteProfessionnel,
    CoteEtudiant,
    CoteLoisirs,
    Realisation,
    SoftKills
  },
};
</script>

<style scoped>
.boxnav{
  display: flex; 
  justify-content: center;
}
a.active {
  background-color: black;
  color: #e1a23f;
  border: 1px solid #e1a23f;
}

nav {
  width: 80%;
  display: flex;
  justify-content: space-between;
  margin-bottom: 4%;
}

a {
  display: flex;
  text-decoration: none;
  background-color: #e1a23f;
  color: black;

  padding: 1%;
  border-radius: 10px;
  width: 17%;
  text-align: center;
  align-items: center;
  justify-content: center;

}

@media screen and (max-width: 767px) {
  nav {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  a {
    width: 100%;
  }
}
</style>