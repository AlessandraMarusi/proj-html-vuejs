<template>
    <div class="cardContainer" :class="{ active: item.isActive }">
        <!-- <img src="../assets/img/Computer-tabs-v2.png" :alt=item.title> -->
        <img :src="require('../assets/img/'+item.img)" alt="">
        <h5>{{item.name}}</h5>
    </div>
</template>

<script>
export default {
    name: "SecondCOmpCards",
    props:['item'],
    computed: {
        imgUrls(){
            return require(this.item.img)
        }
    },
    methods:{
        checkApp(){
            console.log(this.item)
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.cardContainer {
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
    gap: 20px;
    width: calc(100% / 7); 
    height: 200px; 
    box-shadow: 0px 0px 1px 0px #646464;
    img {
        width: 100px;
    }
    h5 {
        color: $txtColorBg;
        font-weight: bolder;
    }
}
.active {
    background-color: $bgColor;
    h5 {
        color: $txtColorOnBg;
    }
    img {
        filter: brightness(0) saturate(100%) invert(93%) sepia(0%) saturate(7500%) hue-rotate(108deg) brightness(107%) contrast(110%);
    }
    
}
</style>