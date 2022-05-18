<template>
    <section class="partners">
        <div class="myContainer">
            <h2>Partners</h2>
            <p>Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy.</p>
            <div class="container iconsContainer">
                <div class="row">
                    <div class="col" v-for="(item, index) in datiPartners" :key="index">
                        <img :src="require('../assets/img/'+item.img)" alt="Icona Partner">
                    </div>
                </div>
            </div>
        </div>
        <div class="waveContainer">
            <img src="../assets/img/background-wave3.png" alt="background wave decoration">
        </div>
    </section>
</template>

<script>
import data from '../dati.json'
export default {
    name: "PartnersComp",
    data(){
        return{
            datiPartners: data.partnersItems
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.partners {
    .myContainer {
        width: 70%;
        margin: 0 auto;
        text-align: center;
        padding: 50px 0;
        p {
            width: 40%;
            margin:  0 auto;
            padding: 30px 0;
        }
        img {
            height: 50px;
            filter: opacity(40%);
        }
    }
    .waveContainer {
        background-color: #F7F8FA;
        overflow: hidden;
        height: 300px;
    }
}
</style>