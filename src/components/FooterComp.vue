<template>
    <div class="container">
      <div class="row">
        <div class="col-md-4 firstCol">
          <img src="../assets/img/theme_eduprime_logo.png" alt="">
          <p>EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
          <div class="socialIcons">
            <button v-for="(item, index) in socialItems" :key="index"><font-awesome-icon :icon="'fa-brands '+item.icon" /></button>
          </div>
        </div>
        <div class="col-md-4 secondCol">
          <div class="listContainer">
            <h4>GetEduPrime</h4>
            <ul>
              <li v-for="(item, index) in firstItems" :key="index">
                <a :href="item.url">{{item.title}}</a>
              </li>
            </ul>
          </div>
          <div class="listContainer">
            <h4>Networking</h4>
            <ul>
              <li v-for="(item, index) in secondItems" :key="index">
                <a :href="item.url">{{item.title}}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-md-4 thirdCol">
          <div class="inputWrapper">
                <input type="email" class="form-control" id="emailInput" aria-describedby="emailHelp" placeholder="Email address...">
                <button class="secBtn"><font-awesome-icon icon="fa-solid fa-magnifying-glass" /></button>
          </div>
          <h5>Search categories</h5>
          <div class="tagsContainer">
            <button v-for="(item, index) in searchItems" :key="index">{{item.title}}</button>
          </div>
          <span>ModelTheme. All rights reserved.</span>
        </div>
      </div>
    </div>
</template>

<script>
import data from '../dati.json'
export default {
    name: 'FooterComp',
  data(){
        return{
            socialItems: data.footerItems.socialList,
            firstItems: data.footerItems.firstList,
            secondItems: data.footerItems.secondList,
            searchItems: data.footerItems.searchList
        }
    },
    methods:{
      check(){
        console.log(this.socialItems)
      }
    }
}
</script>

<style lang="scss">
@import "../style/general";
.firstCol{
  img {
    width: 300px;
    cursor: pointer;
  }
  p{
    padding: 20px 0;
  }
  button {
    background-color: transparent;
    color: $txtColorOnBg;
    border: 2px solid $btnColorSec;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    margin-right: 10px;
    transition: 0.3s;
  }
  button:hover {
    background-color: $btnColorSec;
  }
}
.secondCol {
  display: flex;
  justify-content: space-around;
  h4 {
    font-weight: 900;
    padding-bottom: 25px;
  }
  ul {
    list-style: none;
    padding: 0;
    li {
      margin: 10px 0;
      a {
        transition: 0.5s;
      }
      a:hover {
        color: $txtColorHover;
      }
    }
  }
}
.thirdCol {
  text-align: right;
  .inputWrapper {
    width: 100%;
    position: relative;
    input {
      height: 65px;
      border-radius: 30px;
    }
    button {
      position: absolute;
      top: 50%;
      right: 0%;
      transform: translate(5%, -50%);
      height: 67px;
      width: 67px;
      border-radius: 50%;
    }
  }
  h5 {
    font-weight: 900;
    padding: 40px 0 15px;
  }
  .tagsContainer {
    display: flex;
    justify-content: flex-end;
    flex-wrap: wrap;
    gap: 10px;
    padding-bottom: 20px;
    button {
      background-color: transparent;
      border: 1px solid $white;
      border-radius: 25px;
      padding: 5px 15px;
      color: $txtColorOnBg;
      transition: 00.3s;
    }
    button:hover {
      background-color: $btnColorSec;
    }
  }
  span {
    color: $txtColorHover;
  }
}
</style>