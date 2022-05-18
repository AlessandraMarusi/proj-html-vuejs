<template>
<div class="col-lg-4">
    <div class="myCard">
        <div class="content">
            <h3>{{item.title}}</h3>
            <span>{{item.data}}</span>
            <p>{{item.text}}</p>
        </div>
        <button class="firstBtn smallBtn">+ Find More</button>
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