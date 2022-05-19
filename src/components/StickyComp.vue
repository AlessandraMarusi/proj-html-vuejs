<template>
<div>
    <div class="sideMenu">
        <font-awesome-icon icon="fa-solid fa-cart-shopping" />
        <font-awesome-icon icon="fa-solid fa-book-open" />
        <font-awesome-icon icon="fa-solid fa-life-ring" />
    </div>
    <div class="leftButtons">
        <div class="tooltipContainer">
            <span>Purchase EduPrime on Envato Market</span>
            <div class="triangle">&#9662;</div>
        </div>
        <button class="purchaseBtn">
            <img src="../assets/svg/svg-3.svg" alt="">
            <span>Purchase Theme</span>
        </button>
        <button>
            <img src="../assets/svg/svg-2.svg" alt="">
            <span>Related Themes</span>
        </button>

    </div>
    <a href="#navBar">
        <div class="rightArrow" :class="{myVisible : isVisible}">
            <img src="../assets/img/back-to-top-arrow.svg" alt="">
        </div>
    </a>
</div>
</template>

<script>
export default {
    name: "StickyComp",
    data(){
        return{
            isVisible: false,
            y: window.scrollY
        }
    },
    created () {
    window.addEventListener('scroll', this.handleScroll);
    },
    destroyed () {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods:{
        handleScroll(){
            /* y = window.scrollY */
            this.y = window.scrollY
            if (this.y >= 400) {
                this.isVisible = true
            }
            else {
                this.isVisible = false
            }
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.sideMenu {
    position: fixed;
    left: 0%;
    top: 35%;
    background-color: $btnColorSec;
    color: $txtColorOnBg;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
    border-radius: 0px 10px 10px 0px;
    box-shadow: 0 0 25px rgb(37 37 37 / 40%);
    z-index: 444;
    transition: 00.5s;
    svg {
        padding: 12px;
        cursor: pointer;
        transition: 00.5s;
    }
}
.sideMenu:hover svg{
    padding: 12px 15px;
}
.leftButtons {
    position: fixed;
    left: 2%;
    bottom: 4%;
    z-index: 444;
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    /* justify-content: center; */
    gap: 15px;
    .tooltipContainer {
        width: 170px;
        background-color: #1A1A1A;
        color: $white;
        padding: 5px;
        border-radius: 5px;
        font-size: 00.8rem;
        box-shadow: 0 17px 10px -12px rgba(0, 0, 0, .4);
        text-align: center;
        position: relative;
        .triangle {
            position: absolute;
            bottom: 0%;
            left: 50%;
            transform: translate(-50%, 60%);
            font-size: 2rem;
            color: #1A1A1A;
        }
    }
    button {
        background-color: #454545;
        color: $txtColorOnBg;
        padding: 10px 25px;
        border: none;
        border-radius: 5px;
        box-shadow: 0 17px 10px -12px rgba(0, 0, 0, .4);
        transition: all 0.25s ease-in-out;
        img {
            width: 15px;
        }
        span {
            font-size: 0.8rem;
            padding-left: 5px;
        }
    }
    button:hover {
        background-color:  #d77864;
        transform: translate(0%, -5%);
    }
    .purchaseBtn:hover {
        background-color: #81b441;
        img {
            /* filter: grayscale(100%); */
            filter: contrast(0%);
        }
    }
}
.rightArrow {
    position: fixed;
    bottom: 5%;
    right: 2%;
    background-color: $btnColorSec;
    color: $white;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 444;
    visibility: hidden;
    transition: 00.5s;
}
.rightArrow:hover {
    background-color: $bgColor;
}
.myVisible {
    visibility: visible;
}
</style>