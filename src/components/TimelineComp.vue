<template>
    <section class="timeline">
        <div class="myContainer">
            <img class="icon" src="../assets/img/Clock-and-Bell.png" alt="Icona orologio e campana">
            <h2>University Year</h2>
            <img class="timelineImg" src="../assets/img/Timeline-Item.png" alt="Immagine Timeline">
            <div class="demoTxt timelineTxt">
                <h4>Demo Classes</h4>
                <p>In the first week, students try to accomodate with the teaching style and choose their optional courses.</p>
            </div>
            <div class="graduationTxt timelineTxt">
                <h4>Graduation Day</h4>
                <p>On the day of graduation, all students gather for the ceremony and then network and party among others</p>
            </div>
            <div class="orientationTxt timelineTxt">
                <h4>Orientation</h4>
                <p>First day of the university year, all students gather for the opening ceremony and then network with others.</p>
            </div>
            <div class="evaluationTxt timelineTxt">
                <h4>Evaluation</h4>
                <p>At the end of a semester, students take a general evaluation test for every subject they're learning.</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "TimelineComp"
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.timeline {
    background-color: $bgColor;
    color: $txtColorOnBg;
    height: 700px;
    position: relative;
    overflow: hidden;
    .myContainer {
        width: 70%;
        margin: 0 auto;
        text-align: center;
        h2{
            color: $txtColorOnBg;
        }
        .timelineImg {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        .timelineTxt {
            position: absolute;
            width: 20%;
        }
        .demoTxt {
            top: 22%;
            left: 34%;
        }
        .graduationTxt {
            top: 22%;
            right: 22%;
        }
        .orientationTxt{
            bottom: 20%;
            left: 22%;
        }
        .evaluationTxt {
            bottom: 20%;
            right: 34%;
        }
    }
}
</style>