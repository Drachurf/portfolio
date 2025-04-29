<template>

    <div class="box">
        <div class="contactbox">
            <h3> Mon profil vous plait ? </h3>
            <p>Pour me joindre :</p>
            <div class="contact">
                <div><img src="../assets/images/phone.webp" alt="logo telephone" />
                    <p><a href="tel:0631789951">06 31 78 99 51</a></p>
                </div>
                <div> <img src="../assets/images/mail.png" alt="logo mail" />
                    <p><a href="mailto:fruchard.t@gmail.com">fruchard.t@gmail.com</a></p>
                </div>
                <a href="https://www.linkedin.com/in/thomas-fruchard-a93477252/" target="_blank">
                    <img src="../assets/images/linkedin.svg" alt="logo linkedin" style="border: 1px white solid;" />
                </a>

            </div>
        </div>
    </div>
</template>

<style scoped>
.box {
    display: flex;
    justify-content: center;
    margin-top: 20px;
    flex-direction: column;
    align-items: center;
}

.contact div {
    display: flex;
    align-items: center;
}

.contactbox {
    width: 90%;
    display: flex;
    flex-direction: column;
    margin-top: 20px;
    border-radius: 10px;
    background-color: black;
    color: #e1a23f;
    padding: 5px 20px;
}

a {
    text-decoration: none;
    color: #e1a23f;
}

.contact {
    display: flex;
    justify-content: space-around;
    padding: 0 20px;
}

img {
    border-radius: 25px;
    margin-right: 10px;
    width: 50px;
    height: 50px;
}

@media screen and (max-width: 767px) {
    .contact {
        display: flex;
        flex-direction: column;
        margin-bottom: 3%;
    }
}
</style>