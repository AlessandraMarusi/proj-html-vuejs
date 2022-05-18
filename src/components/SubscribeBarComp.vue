<template>
    <section class="subscribe">
        <div class="myContainer">
            <h3>Subscribe Now to Our Newsletter !</h3>
            <div class="inputWrapper">
                <input type="email" class="form-control" id="emailInput" aria-describedby="emailHelp" placeholder="Email address...">
                <button class="secBtn"><font-awesome-icon icon="fa-solid fa-paper-plane" /></button>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name:"SubscribeBarComp"
}
</script>

<style lang="scss" scoped>
@import "../style/general";
.subscribe {
    background-color: $bgColor;
    .myContainer {
        height: 200px;
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-around;
        align-items: center;
        h3 {
            color: $txtColorOnBg;
            font-weight: 900;
            font-size: 2rem;
        }
        .inputWrapper {
            width: 30%;
            position: relative;
            input {
                height: 65px;
                border-radius: 30px;
            }
            button {
                position: absolute;
                top: 50%;
                right: 0%;
                transform: translate(0%, -50%);
                height: 65px;
                width: 65px;
                border-radius: 50%;
            }
        }
        
    }
}
</style>