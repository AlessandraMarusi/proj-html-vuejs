<template>
    <section>
        <div class="myContainer">
            <h1>Key to your success</h1>
            <p class="my-5">EduPrime is the most versatile WorkdPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
            <button class="secBtn bigBtn mx-4"><font-awesome-icon icon="fa-solid fa-magnifying-glass" />Search courses</button>
            <button class="thirdBtn bigBtn"><font-awesome-icon icon="fa-solid fa-user-plus" />Appry for university</button>
        </div>
        <img class="waveImg" src="../assets/img/Wave-1.png" alt="">
    </section>
</template>

<script>
export default {
    name:'JumboComp'
}
</script>

<style lang="scss" scoped>
@import "../style/general";
section {
    position: relative;
    z-index: 2;
    color: $txtColorOnBg;
    height: 700px;
    overflow: hidden;
    .myContainer {
        width: 40%;
        margin: 0 auto;
        padding-top: 150px;
        text-align: center;
    }
    .waveImg {
        position: absolute;
        bottom: 0%;
        left: 0%;
    }
}
</style>