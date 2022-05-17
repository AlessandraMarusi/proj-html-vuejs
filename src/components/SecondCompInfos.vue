<template>
    <div class="infoContainer">
        <img src="../assets/img/Gavel-Illustration-e1556884768193.png" alt="">
        <div class="txtContainer">
            <h3>Law Faculty</h3>
            <p>Learning from world-leading academics and practitioners, you'll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions</p>
            <button class="firstBtn bigBtn">Read More</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "SecondCompInfos"
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.infoContainer {
    width: 70%;
    margin: 25px auto;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 50px;
    .txtContainer {
        width: 50%;
        h3 {
            font-weight: bolder;
        }
        p {
            width: 80%;
            padding: 25px 0;
        }
    }
}
</style>