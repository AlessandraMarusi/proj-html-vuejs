<template>
    <div class="infoContainer">
        <img :src="require('../assets/img/'+datiCard[activeId].details[0].img)" alt="">
        <div class="txtContainer">
            <h3>{{datiCard[activeId].details[0].title}}</h3>
            <p>{{datiCard[activeId].details[0].description}}</p>
            <button class="firstBtn bigBtn">Read More</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "SecondCompInfos",
    props:['datiCard', 'activeId'],
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.infoContainer {
    width: 70%;
    margin: 25px auto;
    display: flex;
    justify-content: center;
    gap: 50px;
    .txtContainer {
        width: 50%;
        display: flex;
        flex-flow: column;
        justify-content: center;
        align-items: flex-start;
        h3 {
            font-weight: bolder;
        }
        p {
            width: 80%;
        }
    }
}
</style>