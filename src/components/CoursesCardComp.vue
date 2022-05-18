<template>
<div class="col-lg-3">
    <div class="myCard">
        <div class="content">
            <img class="icon" :src="require('../assets/img/'+item.img)" alt="">
            <h3>{{item.title}}</h3>
            <span>{{item.teacher}}</span>
            <span>{{item.price}}</span>
        </div>
        <button class="firstBtn smallBtn">View Course</button>
    </div>
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
        border-radius: 20px;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        box-shadow: 0px 0px 2px 0px #646464;
        .content {
            padding: 50px 25px;
            
            h3 {
                font-weight: 900;
            }
        }
        button {
            position: absolute;
            left: 50%;
            bottom: 0%;
            transform: translate(-50%, 50%);
        }
    }
</style>