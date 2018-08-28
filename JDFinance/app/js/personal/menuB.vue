<template>
    <Panel title="menu" :class="$style.panel">
            <ul :class="$style.content">
                <li>
                    <div>
                   <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9121/110/2300703915/1348/91af205c/59cb613bN1e749e58.png?width=70&height=70" alt="">
                    </div>
                    <p>我的白条</p>
                    <em>> </em>
                </li>
                <li>
                    <div>
                     <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9244/132/2364556535/1134/334cd5d9/59cb612dN5b974dc5.png?width=70&height=70" alt="">
                    </div>
                    <p>我的金条</p>
                    <em>> </em>
                </li>
                <li>
                    <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8014/149/2344686222/2102/341ff316/59cb616bN3e1bd87d.png?width=70&height=70" alt="">
                   </div>
                    <p>我的保障</p>
                    <em>> </em>
                </li>
                <li>
                    <div>
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9649/171/293125950/1453/4cf0cc2/59cb6162N9c71da0f.png?width=70&height=70" alt="">
                    </div>
                    <p>我的众筹</p>
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
                 &:after{
                    content: '';
                    display: inline-block;
                    height: 0;
                    width: 100%;
                    border-bottom: 1px solid #ddd;
                    margin-left: 115px;
                    
                }
                &:last-child:after{
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