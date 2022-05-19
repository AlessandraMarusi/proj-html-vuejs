<template>
    <section id="Jumbotron">
        <!-- <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="false">
            <div class="carousel-inner">
                <div class="carousel-item active">
                <div class="imgFilter"></div>
                    <img src="../assets/img/theme_slider2_bg-1.jpg" class="d-block w-100" alt="Immagine di background">
                    <div class="carousel-caption d-none d-md-block">
                        <h2>Key to your success</h2>
                        <p>EduPrime is the most versatile WorkdPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
                        <button class="secBtn bigBtn mx-4"><font-awesome-icon icon="fa-solid fa-magnifying-glass" />Search courses</button>
                        <button class="thirdBtn bigBtn"><font-awesome-icon icon="fa-solid fa-user-plus" />Appry for university</button>
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="imgFilter"></div>
                    <img src="../assets/img/theme_slider1_bg-1.jpg" class="d-block w-100" alt="Immagine di background">
                    <div class="carousel-caption d-none d-md-block">
                        <h2>Key to your success</h2>
                        <p>EduPrime is the most versatile WorkdPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
                        <button class="secBtn bigBtn mx-4"><font-awesome-icon icon="fa-solid fa-magnifying-glass" />Search courses</button>
                        <button class="thirdBtn bigBtn"><font-awesome-icon icon="fa-solid fa-user-plus" />Appry for university</button>
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="imgFilter"></div>
                    <img src="../assets/img/theme_slider3_bg-1.jpg" class="d-block w-100" alt="Immagine di background">
                    <div class="carousel-caption d-none d-md-block">
                        <h2>Key to your success</h2>
                        <p>EduPrime is the most versatile WorkdPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
                        <button class="secBtn bigBtn mx-4"><font-awesome-icon icon="fa-solid fa-magnifying-glass" />Search courses</button>
                        <button class="thirdBtn bigBtn"><font-awesome-icon icon="fa-solid fa-user-plus" />Appry for university</button>
                    </div>
                </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
        </div> -->
        <!-- <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-inner">
                <div class="carousel-item active">
                <img src="../assets/img/theme_slider2_bg-1.jpg" class="d-block w-100" alt="...">
                </div>
                <div class="carousel-item">
                <img src="../assets/img/theme_slider1_bg-1.jpg" class="d-block w-100" alt="...">
                </div>
                <div class="carousel-item">
                <img src="../assets/img/theme_slider3_bg-1.jpg" class="d-block w-100" alt="...">
                </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
            </div> -->
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
        padding-top: 120px;
        text-align: center;
        h1 {
            font-weight: 900;
            font-size: 3.3rem;
        }
        button {
            margin-top: 20px;
        }
        .secBtn:hover {
            background-color: $btnColorThird;
            color: $txtColorBg;
        }
    }
    .waveImg {
        position: absolute;
        bottom: 0%;
        left: 0%;
    }
}
.imgFilter {
    background-color: $bgColor;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0%;
    left: 0%;
    opacity: 90%;
    z-index: 2;
  }
</style>