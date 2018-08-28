<template>
    <Panel title="生活服务" :class="$style.panel">
        <section>
            <!-- 非数据驱动，写成静态的比较好 -->
            <!-- <div :class="$style.item" v-for="item in items" :key="item.key">
                <router-link :to="{name:'home'}">
                    <img :src="item.src" alt="">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div> -->
            <ul :class="$style.content">
                <li :class="$style.item">
                   <router-link :to="{}">
                        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135"
                            alt="">
                        <p>慧加油</p>
                   </router-link>
                </li>
                <li :class="$style.item">
                    <router-link :to="{}">
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132"
                        alt="">
                    <p>小白信用</p>
                    <p>全新升级</p>
                    </router-link>
                </li>
                <li :class="$style.item">
                    <router-link :to="{}">
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135"
                        alt="">
                    <p>信用卡还款</p>
                    </router-link>
                </li>
                <li :class="$style.item">
                    <router-link :to="{}">
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135"
                        alt="">
                    <p>卡转让</p>
                    </router-link>
                </li>
                <li :class="$style.item">
                    <router-link :to="{}">
                    <img src="https://img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135"
                        alt="">
                    <p>定期还款</p>
                    </router-link>
                </li>
            </ul>
        </section>
    </Panel>
</template>

<script>
    import Panel from '../core/panel.vue'
    export default {
        components: {
            Panel
        },
        data() {
            return {
                items: [{
                        href: 'home',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135',
                        title: '慧加油'
                    },
                    {
                        href: 'home',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132',
                        title: '小白信用'
                    },
                    {
                        href: 'home',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135',
                        title: '信用卡还款'
                    },
                    {
                        href: 'home',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135',
                        title: '卡转让'
                    },
                    {
                        href: 'home',
                        src: '//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135',
                        title: '定期还款'
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" module>
    @import '../../css/element.scss';
    .panel {
        @include panel;
        .content {
            @include flex(row);
            box-sizing: border-box;
            padding-bottom: 40px;
            .item{
                display: inline-block;
                width: 20%;
                //既然让图片居中，也让文字居中
                text-align: center;
                p{
                    text-overflow: ellipsis;
                    white-space: nowrap;
                    overflow: hidden;
                    font-size: 24px;
                    margin-top: 10px;
                    color: #666;
                    &:nth-of-type(2){
                        color: #ff801a;
                    }
                }
                img{
                    width: 90px;
                    height: 90px;
                }
            }
          
        }

    }
</style>