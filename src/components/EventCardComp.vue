<template>
<div class="col-lg-4">
    <div class="myCard">
        <h3>{{item.title}}</h3>
        <span>{{item.data}}</span>
        <p>{{item.text}}</p>
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
        /* margin: 10px; */
    }
</style>