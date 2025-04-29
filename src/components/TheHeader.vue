<template>
  <div class="head">
    <img src="../assets/images/artNumThomas.webp" alt="Logo de Thomas">
    <h1>
      Thomas Fruchard 
    </h1>
    
  </div>
</template>

<style scoped>
.custom-audio-player {
  width: 100%;
  max-width: 400px;
}
.head {
  display: flex;
  margin-bottom: 3%;
  justify-content: space-around;
  align-items: center;
}
img {
  width: 150px;
  height: 150px;
  border-radius: 50% 50% 50% 50% / 50% 50% 50% 50%;
  margin-right: 4%;
}

@media screen and (max-width: 767px){
  .head img{
    width: 75px;
    height: 75px;
  }
  h1{
    font-size: 3em;
  }
}
</style>