<template>
    <Panel title="ln货推荐" :class="$style.panel">
        <section>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t3406/210/2247820735/50952/86016eea/5846d8e7N20446dbd.png?width=750&height=200"
                alt="">
            <div :class="$style.content">
                <div :class="$style.item" v-for="item in tech" :key="item.name">
                    <em>精选</em>
                    <img :src="item.src" alt="">
                    <p>{{item.name}}</p>
                    <h4>
                        <span>￥</span>{{item.price}}
                        <span>起</span>
                    </h4>
                    <article>
                        <div :class="$style.wrapper">
                            <div :class="$style.inner" :style="{width:item.progress+'%'}"></div>
                        </div>
                        <p id="rate">{{item.progress}}%</p>
                    </article>
                </div>
            </div>
        </section>
        <section>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t3739/82/2244582797/54399/746c7d79/5846a953N66b67d05.png?width=750&height=200"
                alt="">
            <div :class="$style.content">
                <div :class="$style.item" v-for="item in intel" :key="item.name">
                    <em>精选</em>
                    <img :src="item.src" alt="">
                    <p>{{item.name}}</p>
                    <h4>
                        <span>￥</span>{{item.price}}&nbsp;
                        <span>起</span>
                    </h4>
                    <article>
                        <div :class="$style.wrapper">
                            <div :class="$style.inner" :style="{width:item.progress+'%'}"></div>
                        </div>
                        <p id="rate">{{item.progress}}%</p>
                    </article>
                </div>
            </div>
        </section>
        <section>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t3406/210/2247820735/50952/86016eea/5846d8e7N20446dbd.png?width=750&height=200"
                alt="">
            <div :class="$style.content">
                <div :class="$style.item" v-for="item in cate" :key="item.name">
                    <em>精选</em>
                    <img :src="item.src" alt="">
                    <p>{{item.name}}</p>
                    <h4>
                        <span>￥</span>{{item.price}}&nbsp;
                        <span>起</span>
                    </h4>
                    <article>
                        <div :class="$style.wrapper">
                            <div :class="$style.inner" :style="{width:item.progress+'%'}"></div>
                        </div>
                        <p id="rate">{{item.progress}}%</p>
                    </article>
                </div>
            </div>
        </section>
    </Panel>
</template>

<script>
    import Panel from '../core/panel.vue'
    export default {
        components: {
            Panel,
        },
        data() {
            return {
                items: [{
                        src: '//img30.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.jpg',
                        name: '双响炮蓝牙音箱',
                        price: 29,
                        type: 'tech',
                        progress:58
                    }, {
                        src: '//img30.360buyimg.com/cf/s250x250_jfs/t15529/308/632300625/135123/adb9c6d0/5a37676dNc31da9ea.jpg',
                        name: '脑波相机',
                        price: 998,
                        type: 'tech',
                        progress:79
                    },
                    {
                        src: '//img30.360buyimg.com/cf/s250x250_jfs/t11257/287/2281727659/55759/e00b90a/5a138f21N32dca834.jpg',
                        name: '智能电动牙刷',
                        price: 19,
                        type: 'intel',
                        progress:170
                    },
                    {
                        src: '//img30.360buyimg.com/cf/s250x250_jfs/t14209/293/662014092/61635/bba5c330/5a33a983N077cac56.jpg',
                        name: '烟草加热电子烟',
                        price: 258,
                        type: 'intel',
                        progress:16
                    },
                    {
                        src: '//img30.360buyimg.com/cf/s250x250_jfs/t15007/47/884045069/149879/17987250/5a3cb182N15868ea1.jpg',
                        name: '赖公高淮封藏老酒',
                        price: 99,
                        type: 'cate',
                        progress:256
                    },
                    {
                        src: '//img30.360buyimg.com/cf/s250x250_jfs/t14197/160/546457496/134173/4e1baccd/5a30ccc5Na44f7492.jpg',
                        name: '泗洪花雕醉蟹',
                        price: 58,
                        type: 'cate',
                        progress:88
                    }
                ]
            }

        },
        computed: {
            tech: function () {
                return this.items.filter(function (item) {
                    item.price = item.price.toFixed(2);
                    return item.type.match(/tech/gi);
                })
            },
            intel: function () {
                return this.items.filter(function (item) {
                    return item.type.match(/intel/gi);
                })
            },
            cate: function () {
                return this.items.filter(function (item) {
                    return item.type.match(/cate/gi);
                })
            },
            // calculateRate() {
            //     var rate = document.querySelector("#rate");

            // }



        }

    }
</script>

<style lang="scss" module>
    @import '../../css/element.scss';
    .panel {
        @include panel;
        >section {
            img {
                width: 100%;
            }
            margin-bottom: 40px;
        }
        .content {
            @include flex(row);
            .item {
                box-sizing: border-box;
                width: 50%;
                position: relative;
                height: 400px;
                text-align: center;
                em {
                    font-size: 20px;
                    display: inline-block;
                    color: #ff0000;
                    padding: 5px;
                    background: linear-gradient(-35deg, #C1C1C1 0, #ACACAC 100%);
                    position: absolute;
                    top: 0;
                    left: 0;
                }
                img {
                    display: inline-block;
                    width: 175px;
                    height: 175px;
                    margin-top: 50px;
                    padding-bottom: 20px;

                }
                p {
                    font-size: 28px;
                }
                h4 {
                    font-size: 36px;
                    color: #ff3232;
                    padding-top: 10px;
                    span:first-child {
                        color: inherit;
                        font-size: 26px;
                    }
                    span:last-child {
                        color: #999;
                        font-size: 20px;
                        margin-left: 4px;
                    }
                }
                article {
                    @include flex(row);
                    align-items: center;
                    justify-content: center;
                    margin-top: 20px;
                    .wrapper {
                        width: 155px;
                        height: 10px;
                        background: #f6e6e6;
                        border-radius: 22px;
                        margin-right: 20px;

                        .inner {
                            width: 80%;
                            max-width: 100%;
                            height: 10px;
                            background-image: linear-gradient(270deg, #f55 1%, #ff9c31 100%);
                            border-radius: 22px;
                        }
                    }
                    P {
                        font-size: 24px;
                        color: #333;
                    }
                }
            }

        }


    }
</style>