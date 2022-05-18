<template>
    <div class="cardContainer" :class="{ active: item.isActive }" @click="changeActive" >
        <img :src="require('../assets/img/'+item.img)" alt="">
        <h5>{{item.name}}</h5>
        <div class="redTriangle" :class="{ activeTriangle: item.isActive }">&#9662;</div>
    </div>
</template>

<script>
export default {
    name: "SecondCOmpCards",
    data(){
        return{
            activeId: 1
        }
    },
    props:['item'],
    methods:{
        changeActive(){
            this.activeId = this.item.id
            /* this.item[this.activeId - 1].isActive = false
            this.item.isActive = true */
            console.log(this.activeId)
            this.$emit('activeIndex', this.activeId);
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
    position: relative;
    cursor: pointer;
    img {
        width: 100px;
    }
    h5 {
        color: $txtColorBg;
        font-weight: bolder;
    }
    .redTriangle {
        color: $bgColor;
        position: absolute;
        bottom: 0%;
        left: 50%;
        transform: translate(-50%, 60%);
        font-size: 80px;
        visibility: hidden;
    }
    .activeTriangle {
        visibility: visible;
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