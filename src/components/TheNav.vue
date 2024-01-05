<template>
    <div class="boxnav">
      <nav>
        <a href="#" @click="showComponent('CoteProfessionnel')">Côté professionnel</a>
        <a href="#" @click="showComponent('CoteEtudiant')">Côté étudiant</a>
        <a href="#" @click="showComponent('CoteLoisirs')">Côté loisirs</a>
      </nav>
  </div>
      <CoteProfessionnel v-if="currentComponent === 'CoteProfessionnel'" />
      <CoteEtudiant v-if="currentComponent === 'CoteEtudiant'" />
      <CoteLoisirs v-if="currentComponent === 'CoteLoisirs'" />
  </template>
  
  <script>
  import CoteProfessionnel from '../pages/CoteProfessionnel.vue';
  import CoteEtudiant from '../pages/CoteEtudiant.vue'; 
  import CoteLoisirs from '../pages/CoteLoisirs.vue';
  
  export default {
    data() {
      return {
        currentComponent: '',
      };
    },
    methods: {
      showComponent(componentName) {
        if(this.currentComponent === componentName){
          this.currentComponent = null;
        }else{
        this.currentComponent = componentName;
      }
    },
    },
    components: {
      CoteProfessionnel,
      CoteEtudiant,
      CoteLoisirs,
    },
  };
  </script>
  
  <style scoped>
  nav {
    display: flex;
    justify-content: space-around;
    margin-bottom: 4%;
  }
  a {
    text-decoration: none;
    background-color: rgba(210, 105, 30, 0.721);
    color: black;
    margin: 1%;
    padding: 2%;
    border-radius: 10px;
    width: 20%;
    text-align: center;
  }
  @media screen and (max-width: 767px){
  nav{
  display: flex;
  flex-direction: column;
  align-items: center;
  }
  a{
  width: 100%;
  }
}
  </style>
  