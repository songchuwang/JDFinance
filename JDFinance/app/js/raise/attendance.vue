<template>
    <Panel title="每日签到" :class="$style.panel">
        <section :class="$style.content">
            <img src="http://img12.360buyimg.com/jrpmobile/jfs/t3184/283/6032981290/37056/fa30c674/589bd5a2Nabdbbbd9.jpg?width=376&height=160"
                alt="">
            <img src="http://img12.360buyimg.com/jrpmobile/jfs/t3298/196/6130416421/33755/a0536d3e/589bd5d4Nf32e7adc.jpg?width=374&height=160"
                alt="">
            <em>不抢白不抢</em>
        </section>
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
    .panel {
        @include panel;
        .content{
            box-sizing: border-box;
            position: relative;
            padding-bottom: 40px;
            @include flex(row);
            >img{
                width: 50%;
                height: 135px;
                display:block;
                margin: 0;      
            }
            em{
                display: inline-block;
                position: absolute;
                font-size: 26px;
                top: -65px;
                right: 25px;
                color: #999;
            }

        }
    }
</style>