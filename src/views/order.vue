<template>
    <div class="orderMain">
        <div class="userImg">
            <img src="../assets//user.jpg" alt="" style="width:250px;height:250px">
        </div>
        <div class="user">
            <div style="font-size: 20px;line-height:2">
                <span>用户名称：</span>
                <span>李天宇</span>
                <br>
                <span>已注册：</span>
                <span>12年</span>
                <br>
                <span>已花费：</span>
                <span>120000元</span>
            </div>
            <div>
                <span style="line-height:3;font-size: 20px;">我的游戏：</span>
                <div class="everyOne">
                    <img src="../assets/dota2.jpg" alt="" style="height:90px;width:90px;">
                    <div style="margin-left:20px;line-height:1.6">
                        <span>游戏名称：</span>
                        <span>DOTA2</span>
                        <br>
                        <span>价格：</span>
                        <span>￥100</span>
                        <br>
                        <span>购买时间：</span>
                        <span>2019-12-16</span>
                    </div>
                </div>
                <div class="everyOne">
                    <img src="../assets/dota2.jpg" alt="" style="height:90px;width:90px;">
                    <div style="margin-left:20px;line-height:1.6">
                        <span>游戏名称：</span>
                        <span>DOTA2</span>
                        <br>
                        <span>价格：</span>
                        <span>￥100</span>
                        <br>
                        <span>购买时间：</span>
                        <span>2019-12-16</span>
                    </div>
                </div>
                <div class="everyOne">
                    <img src="../assets/dota2.jpg" alt="" style="height:90px;width:90px;">
                    <div style="margin-left:20px;line-height:1.6">
                        <span>游戏名称：</span>
                        <span>DOTA2</span>
                        <br>
                        <span>价格：</span>
                        <span>￥100</span>
                        <br>
                        <span>购买时间：</span>
                        <span>2019-12-16</span>
                    </div>
                </div>
                <div class="everyOne">
                    <img src="../assets/dota2.jpg" alt="" style="height:90px;width:90px;">
                    <div style="margin-left:20px;line-height:1.6">
                        <span>游戏名称：</span>
                        <span>DOTA2</span>
                        <br>
                        <span>价格：</span>
                        <span>￥100</span>
                        <br>
                        <span>购买时间：</span>
                        <span>2019-12-16</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
}
</script>
<style lang="scss" scoped>
    .orderMain{
        height: 96%;
        width: 100%;
        padding: 20px 300px;
        box-sizing: border-box;
        display: flex;
        .userImg{
            height: 100%;
            width: 40%;
        }
        .user{
            height: 100%;
            width: 60%;
            .everyOne{
                width: 80%;
                height: 120px;
                background-color: #e4e4e4;
                padding: 15px;
                box-sizing: border-box;
                display: flex;
                margin-bottom: 10px;
            }
        }
    }
    .pointer{
        cursor:pointer;
    }
</style>
