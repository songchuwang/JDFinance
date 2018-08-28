<template>
    <Panel title="menu" :class="$style.panel">
        <ul :class="$style.content">
            <li>
                <div>
                    <img src="../../css/fonts/VIP.svg" alt="">
                </div>
                <p>会员中心</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="../../css/fonts/Bank.svg" alt="">
                </div>
                <p>我的银行卡</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8836/18/2342020923/2120/a9b7a8ff/59cb6124N31cb2889.png?width=70&height=70" alt="">
                </div>
                <p>我的收藏</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8971/199/1863233880/2035/56d04776/59cb5fbdNa7c682c3.png?width=70&height=70"
                        alt="">
                </div>
                <p>我的资产</p>
                <em>> </em>
            </li>
        </ul>
    </Panel>
</template>

<script>
    import Panel from "../core/panel.vue";
    export default {
        components: {
            Panel
        }
    }
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        >h4 {
            display: none;
        }
        .content {
            @include flex(column);
            width: 100%;
            box-sizing: border-box;
            li {
                @include flex(row);
                width: 100%;
                text-align: center;
                justify-content: space-between;
                box-sizing: border-box;
                height: 75px;
                line-height: 75px;
                li:after {
                    content: '';
                    // display: inline-block;
                    height: 0;
                    width: 100%;
                    border-bottom: 1px solid #ddd;
                    margin-left: 115px;

                }
                li:last-child:after {
                    border-bottom: 0;
                }
                >div {
                    height: 75px;
                    widows: 75px;
                    @include flex;
                    align-items: center;
                    justify-content: center;
                    img {
                        display: inline-block;
                        width: 48px;
                        height: 48px;
                        line-height: 48px;
                        padding-left: 20px;

                    }
                }

                p {
                    font-size: 30px;
                    width: 440px;
                    text-align: left;
                    height: 75px;
                }
                em {
                    display: inline-block;
                    box-sizing: border-box;
                    font-size: 32px;
                    margin-right: 20px;
                    color: #999;


                }
            }

        }

    }
</style>