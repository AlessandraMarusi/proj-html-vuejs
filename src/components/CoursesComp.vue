<template>
    <section class="courses">
        <img src="../assets/svg/svg-1.svg" alt="">
        <div class="myContainer">
            <h2>Latest Courses</h2>
            <div class="container">
                <div class="row gx-4">
                    <courses-card-comp :item="item" v-for="(item, index) in datiCourses" :key="index"/>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import data from '../dati.json'
import CoursesCardComp from './CoursesCardComp.vue'
export default {
  components: { CoursesCardComp },
    name: "CoursesComp",
    data(){
        return{
            datiCourses: data.coursesItems
        }
    },
}
</script>

<style lang="scss" scoped>
section {
    @import "../style/general";
    overflow: hidden;
    position: relative;
    > img {
        position: absolute;
        top: -1%;
        left: 0%;
        transform: translate(-2%, 0%);
    }
    .myContainer {
        width: 70%;
        margin: 0 auto;
        padding-top: 100px;
        .container {
            padding: 50px 0;
        }
    }
}
</style>