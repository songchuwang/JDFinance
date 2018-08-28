<template>
    <Panel title="理财精选" :class="$style.panel">
        <div :class="$style.item">     
            <img src="https://img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76" alt="">
            <div>
                <h4>月度理财</h4>
                <p>预期年化收益率4.50%</p>
            </div>
            <router-link :to="{name:''}">
            <em>去赚钱 ></em>
            </router-link>
        </div>
        <div :class="$style.item">
            <img src="https://img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76" alt="">
            <div>
                <h4>季度理财</h4>
                <p>历史年化回报率5.50%</p>
            </div>
            <router-link :to="{name:''}">
            <em>去赚钱 ></em>
            </router-link>
        </div>
        <div :class="$style.item">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76" alt="">
            <div>
                <h4>年度理财</h4>
                <p>历史年化回报率5.80%</p>
            </div>
            <router-link :to="{name:''}">
            <em>去赚钱 ></em>
            </router-link>
        </div>
    </Panel>
</template>

<script>
    import Panel from '../core/panel.vue'
    export default {
        components: {
            Panel,
        }
    }
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel{
    @include panel;
    @include flex(column);
    >h4{
        border-bottom: 1px solid #ddd;
    }
    .item{
        @include flex(row);
        box-sizing: border-box;
        // justify-content: space-around;
        height: 140px;
        align-items: center;
        &:after{
            content: '';
            height: 0;
            width: 100%;
            border-bottom: 1px solid #ddd;
            margin-left: 150px

        }
        &:last-child:after{
            border-bottom: 0;
        }
        img{
            width: 88px;
            height: 88px;
            display: inline-block;
            margin: 0 32px; 
        }
        >div{
            width: 344px;
            h4{
                font-size: 32px;

            }
            p{
                font-size: 24px;
                padding-top: 10px;
                color: #ff5155;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;

            }
        }
        em{
            display: inline-block;
            font-size: 26px;
            color: #ff801a;
            padding: 15px;
        }
    }
}
</style>