<template>
    <div style="height:100%;width:100%">
      <div class="main">
        <div class="iconDiv pointer">
          <span>首页</span>
        </div>
        <div class="pointer" style="width:250px;height:100%;display:flex;">
            <!-- <span class="pointer" @click="backHomepage()">首页</span>
            <div style="width:10px;"></div>
            <span style="color:black">/</span>
            <div style="width:10px;"></div>
            <span class="pointer" @click="order()">我的订单</span>
            <div style="width:10px;"></div>
            <span style="color:black">/</span>
            <div style="width:10px;"></div>
            <span class="pointer" v-if="this.$store.state.loginState === false" @click="login()">您好，请登录</span>
            <span class="pointer" v-if="this.$store.state.loginState === true" @click="logout()">退出登录</span>
            <div style="width:10px;"></div> -->
            <div @click="order()" style="height:100%;width:100px;border-right:1px solid rgb(168, 164, 164);display:flex;align-items:center;justify-content:center">
              个人中心
            </div>
            <div v-if="this.$store.state.loginState === false" @click="login()" style="height:100%;width:150px;border-right:1px solid rgb(168, 164, 164);display:flex;align-items:center;justify-content:center">
              您好，请登录
            </div>
            <div v-if="this.$store.state.loginState === true" @click="logout()" style="height:100%;width:150px;border-right:1px solid rgb(168, 164, 164);display:flex;align-items:center;justify-content:center">
              退出登录
            </div>
        </div>
      </div>
      <router-view></router-view>
    </div>
</template>
<script>
export default {
  name: 'Header',
  data () {
    return {
      state: false
    }
  },
  methods: {
    backHomepage () {
      this.$router.push({ path: '/' })
    },
    order () {
      this.$router.push({ path: '/order' })
    },
    login () {
      this.$router.push({ path: '/login' })
      // console.log(this.$route.name)
    },
    logout () {
      // localStorage.removeItem('token')
      // this.$store.commit('change')
      // console.log(this.$route.name)
      // 如果是在需要登录的页面却退出登录了，那么就要返回到首页
      if (['info', 'order'].indexOf(this.$route.name) > -1) {
        this.$router.push({ path: '/' })
      }
      // 移除token
      localStorage.removeItem('token')
      // 更改了vuex中的登录状态
      this.$store.commit('change')
    }
  }
}
</script>
<style lang="scss" scoped>
    .main{
        width: 100%;
        height: 4%;
        box-sizing: border-box;
        padding: 0 100px;
        background-color: black;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .iconDiv{
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            width:100px;
            border-left: 1px solid rgb(168, 164, 164);
            border-right: 1px solid rgb(168, 164, 164);
        }
        .iconDiv + div{
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            height: 100%;
            width: 100px;
            border-left: 1px solid rgb(168, 164, 164);
            border-right: 1px solid rgb(168, 164, 164);
        }
    }
    .main > span{
        color:rgb(135, 144, 153);
    }
    .pointer{
        cursor:pointer;
    }
</style>
