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
        </div>
        <button>
            <img src="../assets/svg/svg-3.svg" alt="">
            <span>Purchase Theme</span>
        </button>
        <button>
            <img src="../assets/svg/svg-2.svg" alt="">
            <span>Related Themes</span>
        </button>

    </div>
    <div class="rightArrow"></div>
</div>
</template>

<script>
export default {
    name: "StickyComp"
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
    svg {
        padding: 12px;
    }
}
.leftButtons {
    position: fixed;
    left: 2%;
    bottom: 4%;
    z-index: 444;
    display: flex;
    flex-flow: column nowrap;
    gap: 15px;
    button {
        background-color: $titleColor;
        color: $txtColorOnBg;
        padding: 8px 30px;
        border: none;
        border-radius: 5px;
        box-shadow: 0 17px 10px -12px rgba(0, 0, 0, .4);
        img {
            width: 15px;
        }
        span {
            font-size: 0.8rem;
            padding-left: 5px;
        }
    }
}
</style>