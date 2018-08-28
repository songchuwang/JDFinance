<template>
    <Panel title="menu" :class="$style.panel">
        <ul :class="$style.content">
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t10264/48/2521964269/2177/cb479501/59f945edNc1197b64.png?width=90&height=90"
                        alt="">
                </div>
                <p>我的资产</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8836/18/2342020923/2120/a9b7a8ff/59cb6124N31cb2889.png?width=70&height=70"
                        alt="">
                </div>
                <p>我的优惠券</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t10264/48/2521964269/2177/cb479501/59f945edNc1197b64.png?width=90&height=90"
                        alt="">
                </div>
                <p>我的金币</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t12115/250/469950434/3906/ad97c994/5a0bdf3aN22efb724.png?width=90&height=90"
                        alt="">
                </div>
                <p>我的金条</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9244/132/2364556535/1134/334cd5d9/59cb612dN5b974dc5.png?width=70&height=70"
                        alt="">
                </div>
                <p>我的借钱</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9121/110/2300703915/1348/91af205c/59cb613bN1e749e58.png?width=70&height=70"
                        alt="">
                </div>
                <p>我的白条</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9649/171/293125950/1453/4cf0cc2/59cb6162N9c71da0f.png?width=70&height=70"
                        alt="">
                </div>
                <p>我的众筹</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8014/149/2344686222/2102/341ff316/59cb616bN3e1bd87d.png?width=70&height=70"
                        alt="">
                </div>
                <p>我的保障</p>
                <em>> </em>
            </li>
            <li :class="$style.item_realname">
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t10423/230/287832134/1427/af7e4c86/59cb61b2N53280a30.png?width=70&height=70"
                        alt="">
                </div>
                <p>实名认证</p>
                <em>> </em>
            </li>
            <li :class="$style.item_help">
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9832/294/292213011/2420/30888b3d/59cb61c9Nc2bbc057.png?width=70&height=70"
                        alt="">
                </div>
                <p>帮助中心</p>
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
            background: #f5f5f5;
            li {
                @include flex(row);
                width: 100%;
                text-align: center;
                justify-content: space-between;
                box-sizing: border-box;
                height: 75px;
                line-height: 75px;
                background: #fff;
                li:after {
                    content: '';
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
            .item_realname,
            .item_help {
                margin-top: 20px;
            }

        }

    }
</style>