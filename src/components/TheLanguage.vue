<template>
    <div class="boxlanguage">
        <button @click="toggleLangage">
            <img src="../assets/logo/html5.svg" alt="Logo Html">
            <img src="../assets/logo/css3-alt.svg" alt="Logo CSS">
            <img src="../assets/logo/vuejs.svg" alt="Logo VUE">
            <img src="../assets/logo/react.svg" alt="Logo React">
            <img src="../assets/logo/angular.svg" alt="Logo Angular">
            <img src="../assets/logo/square-js.svg" alt="Logo JavaScript">
            <img src="../assets/logo/php.svg" alt="Logo PHP">
            <img src="../assets/logo/node-js.svg" alt="Logo NodeJs">
            <img src="../assets/logo/database-solid.svg" alt="Logo SQL">
        </button>
    </div>
    <div v-if="afficherLangage">
        <h2>Maitrise : </h2>
        <div class="langage">
                <img class="imgLang" src="../assets/images/artNumThomas.webp" alt="On dirait moi">
            <div class="boxLang">
                <div class="flexBet"><p>Html</p><p><strong class="gold">- - - - -</strong></p></div>
                <div class="flexBet"><p>CSS</p><p><strong class="gold">- - - - -</strong></p></div>
                <div class="flexBet"><p>VueJs</p><p><strong class="gold">- - -</strong> - -</p></div>
                <div class="flexBet"><p>React</p><p><strong class="gold">- -</strong> - - -</p></div>
                <div class="flexBet"><p>JavaScript</p><p><strong class="gold">- - - -</strong> -</p></div>
                <div class="flexBet"><p>Php</p><p><strong class="gold">- - -</strong> - -</p></div>
                <div class="flexBet"><p>NodeJs</p><p><strong class="gold">- - -</strong> - -</p></div>
                <div class="flexBet"><p>SQL (MySql / Postgre)</p><p><strong class="gold">- -</strong> - - -</p></div>
                <div class="flexBet"><p>MongoDB</p><p><strong class="gold">-</strong> - - - -</p></div>
            </div>
            <!-- <ul class="maitrise">
                
                <li><strong class="gold">- - - - -</strong></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul> -->
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            afficherLangage: false
        };
    },
    methods: {
        toggleLangage() {
            this.afficherLangage = !this.afficherLangage;
        }
    },
}
</script>

<style scoped>
.boxlanguage {
    display: flex;
    justify-content: center;
    margin-top: 20px;
    flex-direction: column;
    align-items: center;
}
.gold {
    color: goldenrod;
}
.imgLang {
    width: 30%;
    height: 60%;
    display: block;
    margin: 0 0;
}
button {
    border: 5px solid rgba(210, 105, 30, 0.721);
    cursor: pointer;
    background: white;
    padding: 1%;
    width: 95%;
    border-radius: 10px;
}
.boxLang{
    width: 50%;
}
.langage {
    display: flex;
    justify-content: space-around;
    font-size: x-large;
}
.maitrise {
    list-style-type: none;
}
button img {
    background-color: white;
    width: 60px;
    height: 60px;
}
li{
    display: flex;
    justify-content: space-between;
    margin-right: 2%;
}
.flexBet{
    display: flex;
    justify-content: space-between;
}
.flexBet p {
    margin: 5px;
}

@media screen and (max-width: 767px){
  .imgLang{
    display: none;
  }
  .boxLang{
    width: 100%;
  }
}
</style>