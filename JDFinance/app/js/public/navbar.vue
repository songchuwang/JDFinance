<template>
    <Panel :class="$style.panel">
            <ul :class="$style.content">
                <li>
                    <router-link :to="{name:'home'}">
                    <i class="icon-home"></i>
                    <p>首页</p>
                    </router-link>
                </li>
                <li>
                    <router-link :to="{name:'money'}">
                    <i class="icon-coin-yen"></i>
                    <p>理财</p>
                    </router-link>
                </li>
                <li>
                    <router-link :to="{name:'blank'}">
                    <i class="icon-file-text2"></i>
                    <p>白条</p>
                    </router-link>
                </li>
                <li>
                    <router-link :to="{name:'raise'}">
                    <i class="icon-compass"></i>
                    <p>众筹</p>
                    </router-link>
                </li>
                <li>
                     <router-link :to="{name:'personal'}">
                    <i class="icon-user"></i>
                    <p>我的</p>
                    </router-link>
                </li>
            </ul>
    </Panel>
</template>

<script>
import Panel from '../core/panel.vue';

    export default {
        components:{
            Panel
        }

    }
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel{
    @include panel;
    margin: 0 !important;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    height: 100px;
    z-index: 100;
    box-sizing: border-box;
   
    >h4{
        display: none;
    }
    .content{
        @include flex(row);
        padding: 10px 0;
        box-sizing: border-box;
        justify-content: space-around;
        margin: 0;
        li{
            width: 20%;
            display: inline-block;
            text-align: center;
            box-sizing: border-box;
            i{
                width: 44px;
                height:44px;
                display: inline-block;
                color: #666;

            }
            p{
                font-size: 22px;
                color: #666;
                padding: 8px 0;
            }
        }
    }
}

</style>
