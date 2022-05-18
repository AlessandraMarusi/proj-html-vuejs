<template>
<section class="infos">
    <div class="myContainer">
        <div class="content">
            <div class="txt">
                <img class="icon" src="../assets/img/Exam-icon.png" alt="Icona esame">
                <h2>The most efficient examination method</h2>
                <p>EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.</p>
                <button class="firstBtn bigBtn">Discover the Method</button>
            </div>
            <img src="../assets/img/Exam-Illustration.png" alt="Illustrazione esame">
        </div>
        <div class="content">
            <img src="../assets/img/Girl-Illustration.png" alt="Illustrazione ragazza">
            <div class="txt">
                 <img class="icon" src="../assets/img/Exam-icon-1.png" alt="Icona esame">
                <h2>Variable fees for international students</h2>
                <p>EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.</p>
                <button class="firstBtn bigBtn">List of Fees</button>
            </div>
        </div>

    </div>
</section>
</template>

<script>
export default {
    name: "InfoComp "
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.myContainer {
    width: 70%;
    margin: 0 auto;
    .content {
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 50px 0;
        .txt {
            width: 40%;
        }
        >img {
        height: 350px;
        }
    }
}
</style>