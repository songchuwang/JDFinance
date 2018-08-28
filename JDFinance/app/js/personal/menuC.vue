<template>
    <Panel title="menu" :class="$style.panel">
        <ul :class="$style.content">
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t10423/230/287832134/1427/af7e4c86/59cb61b2N53280a30.png?width=70&height=70"
                        alt="">
                </div>
                <p>实名认证</p>
                <em>> </em>
            </li>
            <li>
                <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9832/294/292213011/2420/30888b3d/59cb61c9Nc2bbc057.png?width=70&height=70" alt="">
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

            li {
                @include flex(row);
                width: 100%;
                text-align: center;
                justify-content: space-between;
                box-sizing: border-box;
                height: 75px;
                line-height: 75px;
                &:after {
                    content: '';
                    display: inline-block;
                    height: 0;
                    width: 100%;
                    border-bottom: 1px solid #ddd;
                    margin-left: 115px;

                }
                &:last-child:after {
                    border-bottom: none;
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