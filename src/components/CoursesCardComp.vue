<template>
<div class="col-lg-3">
    <div class="myCard">
        <div class="content">
            <img class="icon" :src="require('../assets/img/'+item.img)" alt="">
            <a href="#"><h5>{{item.title}}</h5></a>
            <p><font-awesome-icon icon="fa-regular fa-user" /> Teacher: <span class="bolder">{{item.teacher}}</span></p>
            <p><font-awesome-icon icon="fa-regular fa-money-bill-1" /> Price: <span class="bolder">{{item.price}}</span></p>
        </div>
    </div>
    <button class="firstBtn smallBtn"><font-awesome-icon icon="fa-regular fa-eye" /> View Course</button>
</div>
</template>

<script>
export default {
    name:"EventCardComp",
    props:['item'],
}
</script>

<style lang="scss" scoped>
@import "../style/general";
    .myCard {
        background-color: $white;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        box-shadow: 0px 0px 10px 0px #d6d2d2;
        text-align: center;
        .content {
            padding: 30px 0px;
            .icon {
                width: 70px;
                transition: 0.5s;
            }
            .icon:hover {
                transform: scale(1.1);
            }
            a {
                color: $titleColor;
                h5 {
                font-weight: 900;
                }
            }
            a:hover {
                color: $txtColorBg;
            }
        }
    }
    .col-lg-3 {
        position: relative;
        button {
            position: absolute;
            bottom: 0%;
            left: 50%;
            transform: translate(-50%, 50%);
            min-width: 50%;
        }
    }
    .bolder {
        font-weight: bolder;
    }
</style>