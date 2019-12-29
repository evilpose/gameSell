<template>
  <div class="homePage">
    <div class="mainDiv">
      <!-- 轮播图 -->
      <div class="carousel">
        <el-carousel :interval="4000" type="card" height="400px">
          <el-carousel-item v-for="(item ,index) in imgList" :key="index">
            <img :src = item.img alt="" style="height:100%;width:100%">
          </el-carousel-item>
        </el-carousel>
      </div>
      <!-- 搜索栏 -->
      <div class="search">
        <div>
          <input type="text">
          <div class="pointer">搜索</div>
        </div>
      </div>
      <!-- 推荐专区 -->
      <div class="recommend">
        <div class="top">
          推荐
          <div style="height:1px;background-color:white;width:95%"></div>
        </div>
        <div class="bottom">
          <!-- 最多只能放8个 -->
          <img class="pointer" @click="into()" src="../assets/Advertisement-3.jpg">
          <img class="pointer" src="../assets/Advertisement-1.jpg">
          <img class="pointer" src="../assets/Advertisement-2.jpg">
          <img class="pointer" src="../assets/Advertisement-3.jpg">
          <img class="pointer" src="../assets/Advertisement-1.jpg">
          <img class="pointer" src="../assets/Advertisement-2.jpg">
          <img class="pointer" src="../assets/Advertisement-3.jpg">
        </div>
      </div>
      <img src="../assets/base.png" style="width:100%">
      <div class="activity">
        <div>
          <img src="../assets/hero.png" >
          <div style="width:200px;height:25px">
            <span class="reduce">-75% </span>
            <span class="original"> ￥199 </span>
            <span class="now">￥100</span>
          </div>
        </div>
        <div>
          <img src="../assets/hero_2.png" >
          <div style="width:200px;height:25px">
            <span class="reduce">-75% </span>
            <span class="original"> ￥199 </span>
            <span class="now">￥100</span>
          </div>
        </div>
        <div>
          <img src="../assets/hero_3.png" >
          <div style="width:200px;height:25px">
            <span class="reduce">-75% </span>
            <span class="original"> ￥199 </span>
            <span class="now">￥100</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>s
<script>
// import axios from 'axios'
export default {
  name: 'homePage',
  components: {
  },
  data () {
    return {
      imgList: [
        { img: require('../assets/Advertisement-1.jpg') },
        { img: require('../assets/Advertisement-2.jpg') },
        { img: require('../assets/Advertisement-3.jpg') }
      ]
    }
  },
  methods: {
    into () {
      this.$router.push({ path: '/info' })
    }
  },
  created () {
  }
}
</script>
<style lang="scss" scoped>
  .homePage{
    width: 100%;
    height: 96%;
    background-color: rgb(38, 49, 43);
    background-image: url('../assets/homebg.gif');
    background-size:100% 100%;
  }
  .mainDiv{
    width: 100%;
    height: 100%;
    .carousel{
      height: 70%;
      width: 100%;
      padding: 80px 100px 0 100px;
      box-sizing: border-box;
    }
    .search{
      height: 30%;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      div{
        height: 20%;
        width: 400px;
        display: flex;
        div{
          height:100%;width:30%;background-color:rgb(116, 206, 159);color:white;border-radius:0 10px 10px 0;
          display: flex;justify-content: center;align-items: center;
        }
        input{
          height: 100%;
          width: 70%;
          outline: none;
          border-radius: 10px 0 0 10px;
          border:none;
          padding: 0 10px;
        }
      }
    }
    .recommend{
      height: 500px;
      width: 100%;
      padding: 40px 150px 0 150px;
      box-sizing: border-box;
      font-size: 20px;
      color: white;
      background-color: #3A5059;
      .top{
        height:10px;width:100%;display:flex;align-items:center;justify-content:space-between;margin-bottom:20px
      }
      .bottom{
        height:430px;width:100%;display:flex;flex-wrap:wrap;justify-content:space-around;align-content:flex-start;
        img{
          width:250px;height:150px;margin-bottom:20px;box-shadow: 0 0 10px black;
        }
        img:hover{
          width:255px;height:155px;margin-bottom:15px;box-shadow: 0 0 10px black;
        }
      }
    }
  }
  .pointer{
    cursor: pointer;
  }
  .activity{
    height:600px;width:100%;background-color:#3A5059;
    padding: 40px 200px 150px 200px;
    box-sizing: border-box;
    display: flex;
    img{
      height:410px;
      width: 350px;
      box-shadow: 0 0 10px black;
      margin-right:30px;
    }
    img:hover{
      height:415px;
      width: 355px;
      box-shadow: 0 0 10px black;
      margin-right:25px;
    }
    .reduce{
      background-color:rgb(149, 185, 16);
    }
    .original{
      background-color:black;color:#ccc;text-decoration:line-through #ccc;
    }
    .now{
      background-color:black;color:white;
    }
  }
</style>
<style>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
  }
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>
