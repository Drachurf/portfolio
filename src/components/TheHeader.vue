<template>
  <div class="head">
    <h1>
      Thomas
    </h1>
    <img src="../assets/images/logoT2F.webp" alt="Logo de Thomas">
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
  justify-content: space-between;
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