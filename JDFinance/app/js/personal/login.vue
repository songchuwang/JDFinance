<template>
    <Panel title="立即登录" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.login">
                <div :class="$style.head">
                   <img src="https://img12.360buyimg.com/jrpmobile/jfs/t2644/238/1420176553/1442/96e2885/573d96deN06201af5.png" alt="">
                </div>
                 <!-- <img src="../../css/fonts/head.jpg" alt=""> -->
                <div :class="$style.tip">
                    <h4>立即登录</h4>
                    <p>首次登录，领取888元大礼包</p>
                </div>
                <em>> </em>
            </div>
            <ul :class="$style.daily">
                <li>
                    <i class="icon-pencil"></i>
                    <p>签到</p>
                </li>
                <li>
                    <i class="icon-sun"></i>
                    <p>早起打卡</p>
                </li>
                <li>
                    <i class="icon-calendar"></i>
                    <p>日历</p>
                </li>
                <li>
                    <i class="icon-list2"></i>
                    <p>任务</p>
                </li>
            </ul>

        </section>
    </Panel>
</template>

<script>
    import Panel from "../core/panel.vue";
    export default {
        components: {
            Panel,
        }
    }
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel; // background: #f5f5f5;
        margin: 0 !important;
        >h4 {
            display: none;
        }
        .content {
            @include flex; // background: #f5f5f5;
            box-sizing: border-box; // justify-content: center;
            align-items: center;
            width: 100%;
            .login {
                @include flex(row);
                width: 100%;
                height: 150px;
                box-sizing: border-box;
                align-items: center;
                border-bottom: 1px solid #ddd;
                .head {
                    overflow: hidden;
                    width: 95px;
                    height: 95px;
                    background: #ddd;
                    border-radius: 50px;
                    margin: 0 20px;
                    text-align: center;
                    >img{
                        width: 95px;
                        height: 95px;
                    }
                }
                .tip {
                    width: 450px;
                    h4 {
                        font-size: 28px;
                        font-weight: 600;
                    }
                    p {
                        height: 40px;
                        line-height: 40px;
                        font-size: 24px;
                        color: #EE661A;
                    }
                }
                em{
                    font-size: 28px;
                    color: #999;
                }


            }
            .daily {
                @include flex(row);
                width: 100%;
                padding: 30px 0;
                justify-content: space-around;
                li {
                    width: 25%;
                    display: inline-block;
                    text-align: center;
                    p {
                        font-size: 24px;
                    }
                    i {
                        font-size: 30px;
                        width: 80px;
                        height: 80px;
                        line-height: 80px;
                        display: inline-block;
                        border-radius: 45px;
                        color: #fff;
                        margin-bottom: 10px;


                    }
                    &:nth-child(1) {
                        i {
                            background-color: #FF5A57;

                        }
                    }
                    &:nth-child(2) {
                        i {
                            background-color: #FF7B00;
                            font-size: 40px;

                        }
                    }
                    &:nth-child(3) {
                        i {
                            background-color: #2175FF;

                        }
                    }
                    &:nth-child(4) {
                        i {
                            background-color: #4CAD49;

                        }
                    }

                }


            }

        }
    }
</style>