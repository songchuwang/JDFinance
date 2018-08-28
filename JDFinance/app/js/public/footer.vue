<template>
    <Panel :class="[$style.panel,cname]">
        <section :class="$style.content">
            <div :class="$style.help">
                <router-link :to="{}">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252"
                        alt="">
                </router-link>
            </div>
            <ul :class="$style.type">
                <li>
                    <i class="icon-mobile2"></i>
                    <p>客户端</p>
                </li>
                <li>
                    <i class="icon-tablet"></i>
                    <p>触屏版</p>
                </li>
                <li>
                    <i class="icon-display"></i>
                    <p>电脑版</p>
                </li>
            </ul>
            <ul :class="$style.copyright">
                <li>
                    <p>Copyright © 2004-2017 京东JD.com 版权所有</p>
                </li>
                <li>
                    <p>投资有风险，购买需谨慎</p>
                </li>
                <li>
                    <p>京东金融平台服务协议</p>
                </li>
            </ul>
        </section>
    </Panel>

</template>

<script>
    import Panel from '../core/panel';
    export default {
        components: {
            Panel,
        },
        props: {
            cname: {
                type: String,
                default: ''
            }
        }

    }
</script>

<style lang="scss" module>
    @import '../../css/element.scss';
    .panel {
        @include panel;
        margin-bottom: 100px;
        >h4 {
            display: none;
        }
        .content {
            @include flex(column);
            box-sizing: border-box;
            ul {
                background-color: #F5F5F5;
            }
            .help {
                width: 100%;
                img {
                    width: 100%;
                }
            }
            .type {
                @include flex(row);
                padding: 20px 0 0px 0;
                box-sizing: border-box;
                border-bottom: 1px solid #ddd;
                li {
                    width: 33.33%;
                    display: inline-block;
                    box-sizing: border-box;
                    text-align: center;
                    i {
                        margin-top: 20px;
                        font-size: 55px;
                        color: #666;
                        width: 80px;
                        height: 80px;
                        display: inline-block;
                    }
                    p {
                        font-size: 26px;
                        color: #999;
                        padding-bottom: 30px;
                    }
                }

            }
            .copyright {
                @include flex(column);
                li {
                    font-size: 24px;
                    text-align: center;
                    padding: 30px 0;
                    color: #999;
                    border-bottom: 1px solid #ddd;
                }
            }
        }

    }
</style>