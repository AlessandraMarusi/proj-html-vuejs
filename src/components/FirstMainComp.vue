<template>
    <section class="firstSection">
        <!-- <img class="bgImg" src="../assets/img/home-background.png" alt="decorazione di background"> -->
        <div class="myContainer">
            <div class="txtContainer">
                <img class="icon" src="../assets/img/Books-icon.png" alt="Icona libri">
                <h2>Thousands of courses for any type of student</h2>
                <p>At EduPrime, it doesn't matter what domain you wish to pursue a career in. Here you can find a course that satifies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides.</p>
                <button class="secBtn bigBtn">Browse through courses</button>
            </div>
            <img src="../assets/img/Graduation-Illustration.png" alt="Illustrazione cappello da laureato">
        </div>
    </section>
</template>

<script>
export default {
    name: "FirstMainComp"
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.firstSection {
    margin: 20px 0;
    height: 700px;
    display: flex;
    align-items: center;
    background-image: url("../assets/img/home-background.png");
    background-size: contain;
    background-repeat: no-repeat;
    .myContainer {
    display: flex;
    width: 70%;
    margin: 0 auto;
    justify-content: space-around;
    .txtContainer {
        position: relative;
        width: 50%;
        color: $titleColor;
        .icon {
            height: 50px;
            width: 50px;
            position: absolute;
            top: -50px;
            left: 0%;
        }
        p {
            padding: 30px 0;
        }
        button {
            font-weight: bolder;
        }
    }
        
        img {
            width: 450px;
        }
    }
}

</style>