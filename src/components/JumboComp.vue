<template>
    <section>
        <div class="myContainer">
            <h1>Key to your success</h1>
            <p>EduPrime is the most versatile WorkdPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
            <button class="firstBtn bigBtn"><font-awesome-icon icon="fa-solid fa-magnifying-glass" />Search courses</button>
            <button class="thirdBtn bigBtn"><font-awesome-icon icon="fa-solid fa-user-plus" />Appry for university</button>
        </div>
    </section>
</template>

<script>
export default {
    name:'JumboComp'
}
</script>

<style lang="scss">
@import "../style/general";
section {
    position: relative;
    z-index: 2;
    color: $txtColorOnBg;
}
</style>