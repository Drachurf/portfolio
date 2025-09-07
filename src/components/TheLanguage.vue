<template>
    <hr>
    <h2>Hard Skills : </h2>
    <div class="boxlanguage">
        <button @click="toggleLangage">
            <img src="../assets/logo/python.svg" alt="Logo Python">
            <img src="../assets/logo/html5.svg" alt="Logo Html">
            <img src="../assets/logo/css3-alt.svg" alt="Logo CSS">
            <img src="../assets/logo/vuejs.svg" alt="Logo VUE">
            <img src="../assets/logo/square-js.svg" alt="Logo JavaScript">
            <img src="../assets/logo/php.svg" alt="Logo PHP">
            <img src="../assets/logo/node-js.svg" alt="Logo NodeJs">
            <img src="../assets/logo/database-solid.svg" alt="Logo SQL">
        </button>
    </div>
    <div v-if="afficherLangage">
        <div class="langage">
            <div>
                <div class="flexBet">
                    <p>Python</p>
                    <p><strong class="gold">- - - -</strong> -</p>
                </div>
                <div class="flexBet">
                    <p>NodeJs</p>
                    <p><strong class="gold">- - -</strong> - -</p>
                </div>
                <div class="flexBet">
                    <p>JavaScript</p>
                    <p><strong class="gold">- - - -</strong> -</p>
                </div>
                <div class="flexBet">
                    <p>MongoDB</p>
                    <p><strong class="gold">-</strong> - - - -</p>
                </div>
                <div class="flexBet">
                    <p>Alteryx</p>
                    <p><strong class="gold">- - - -</strong> -</p>
                </div>
            </div>
            <div>
                <div class="vertical-divider"></div>
            </div>
            <div class="boxLang">
                <div class="flexBet">
                    <p>Php</p>
                    <p><strong class="gold">- - -</strong> - -</p>
                </div>
                <div class="flexBet">
                    <p>Html</p>
                    <p><strong class="gold">- - - - -</strong></p>
                </div>
                <div class="flexBet">
                    <p>CSS</p>
                    <p><strong class="gold">- - - - -</strong></p>
                </div>
                <div class="flexBet">
                    <p>VueJs</p>
                    <p><strong class="gold">- - -</strong> - -</p>
                </div>

                <div class="flexBet">
                    <p>SQL (MySql / PostgreSQL / Oracle)</p>
                    <p><strong class="gold">- - - -</strong> -</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            afficherLangage: true
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
    color: #e1a23f;
}

.imgLang {
    width: 30%;
    height: 60%;
    display: block;
    margin: 0 0;
}

button {
    border: 5px solid #e1a23f;
    cursor: pointer;
    background: white;
    padding: 1%;
    width: 95%;
    border-radius: 10px;
    margin-bottom: 5%;
}

.boxLang {
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

li {
    display: flex;
    justify-content: space-between;
    margin-right: 2%;
}

.vertical-divider {
    width: 2px;
    height: 100%;
    background-color: #e1a23f;
    ;
    margin: 0 20px;
}

.flexBet {
    display: flex;
    justify-content: space-between;
}

.flexBet p {
    margin: 5px;
}

@media screen and (max-width: 767px) {
    .boxLang {
        width: 100%;
    }
    .flexBet{
        font-size: medium;
    }
    .langage {
    display: flex;
    flex-direction: column;
}
.vertical-divider{
    display: none;
}
}
</style>