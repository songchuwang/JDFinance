<template>
    <Panel title="白条福利" :class="$style.panel">
        <div :class="$style.item">
            <img src="https://img12.360buyimg.com/jrpmobile/jfs/t4378/62/155957680/9017/16463551/58affd58Nb5c9198e.jpg?width=120&height=120" alt="">
            <div>
                <h4>开通白条</h4>
                <p>送188元礼包</p>
            </div>
            <em>立即开通 > </em>
        </div>
        <div :class="$style.item">
            <img src="https://img12.360buyimg.com/jrpmobile/jfs/t4150/330/141981421/9147/604e3e04/58affc3bNbfa8f9d7.jpg?width=120&height=120" alt="">
            <div>
                <h4>白条闪付</h4>
                <p>新手享158元礼包</p>
            </div>
            <em>立即开通 > </em>
        </div>
        <div :class="$style.item">
            <img src="https://img12.360buyimg.com/jrpmobile/jfs/t4270/96/1102370053/8651/58b7fa5a/58bd2e10N453e9464.jpg?width=120&height=120" alt="">
            <div>
                <h4>白条提额</h4>
                <p>金融app专享提额礼包</p>
            </div>
            <em>去提额 > </em>
        </div>

    </Panel>
</template>

<script>
    import Panel from '../core/panel.vue';
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
    box-sizing: border-box;
    >h4{
        border-bottom: 1px solid #ddd;
    }
    .item{
        box-sizing: border-box;
        @include flex(row);
        align-items: center;
        height: 140px;
        white-space: nowrap;
        img{
            display: inline-block;
            width: 88px;
            height: 88px;
            margin: 0 32px;
        }
        >div{
            box-sizing: border-box;
            width: 300px;
            h4{
                font-size: 32px;
                color: #2b2b2b;
                padding-top: 5px;
            }
            p{
                font-size: 24px;
                color: #666;
                padding-top: 15px;
                text-overflow: ellipsis;
                white-space: nowrap;
                overflow: hidden;
            }

        }
        em{
            font-size: 28px;
            color: #ff801a;
            display: inline-block;
            padding: 20px;
        }

    }
}
</style>