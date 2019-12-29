<template>
    <div class="infomain">
      <div class="main">
        <div class="top">
          <img src="../assets/destiny2.jpg" alt="" style="height:300px;width:300px">
          <div style="font-size:20px;margin-left:20px;line-height:2">
            <span>游戏名称：destiny2</span>
            <br>
            <span>价格：</span>
            <span style="color:red">￥200</span>
            <br>
            <span>发行日期：2200-12-12</span>
            <br>
            <span>人数：单人</span>
            <br>
            <span>类型：角色扮演</span>
          </div>
          <div class="btn pointer" @click="buy()">购买</div>
        </div>
        <div class="bottom">
          <span style="line-height:2">概述：</span>
          <div>
            极乐迪斯科（Disco Elysium）》是一款极具创新性的开放世界RPG。扮演身怀绝技的警探，穿梭在城市街区间，谱写属于自己的篇章。讯问那些让你无法忘却的角色，勘破凶案，或是受贿沉沦。当英雄，还是做败类，由你来定。
          </div>
          <br>
          <img src="../assets/Advertisement-1.jpg">
          <img src="../assets/lang1.jpg">
        </div>
      </div>
    </div>
</template>
<script>
export default {
  name: 'info',
  components: {
  },
  data () {
    return {
    }
  },
  methods: {
    buy () {
      this.$confirm('是否花费 200元 购买游戏 destiny2 ?', '提示', {
        confirmButtonText: '确定',
        cancelButtonText: '取消',
        type: 'warning',
        lockScroll: false
      }).then(() => {
        this.$message({
          type: 'success',
          message: '购买成功!'
        })
      }).catch(() => {
        this.$message({
          type: 'info',
          message: '已取消购买'
        })
      })
    }
  }
}
</script>
<style lang="scss" scoped>
  .infomain{
    height: 96%;
    width: 100%;
    padding: 0 250px;
    box-sizing: border-box;
    .main{
      // height: 100%;
      width: 100%;
      background-color: #f1f0f0;
      padding: 40px 20px;
      box-sizing: border-box;
      .top{
        height: 300px;
        width: 100%;
        display: flex;
        .btn{
          height: 40px;
          width: 100px;
          background-color: coral;
          border-radius: 5px;
          color: white;
          display: flex;
          justify-content: center;
          align-items: center;
          align-self: flex-end;
          margin-left: 300px;
        }
      }
      .bottom{
        // height: 500px;
        width: 100%;
        margin-top: 20px;
        img{
          width:600px;height:300px;margin-bottom:10px
        }
      }
    }
  }
  .pointer{
    cursor: pointer;
  }
</style>
