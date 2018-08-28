<template>
    <Panel title="下载APP" :class="$style.panel">
        <section :class="$style.content">
            <div></div>
            <p>立即下载</p>
            <span>Copyright © 2018 京东JD.com 版权所有</span>       
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
    html,
    body {
        background: #fff;
    }
.panel {
        @include panel;
        margin: 0 !important;

        >h4 {
            display: none;
        }
        .content {
            @include flex;
            align-items: center;
            justify-content: center;
            height: 1124px;
            width: 100%;
            >div{
                background: url(http://img12.360buyimg.com/jrpmobile/jfs/t8956/285/1249806938/50853/8cd3c8f0/59b65f36N05367075.png) center center no-repeat;
                width: 600px;
                height: 600px;
                background-size: 100% auto;
                margin-top: -400px;

            }
            >p{
                @include btn($size:32px, $color:#fff, $bgcolor:#f14431, $padding:5px, $radius:5px);
                height: 80px;
                line-height: 80px;
                width: 460px;
                background-image: linear-gradient(270deg,#f55c33 0,#ee2d1b 75%);
                box-shadow: 0 12px 32px 0 rgba(255,159,135,.6);
                position: fixed;
                bottom: 130px;

            }
            >span{
                font-size: 18px;
                position: fixed;
                bottom: 40px;
                color: #999;
            }
           
        }

    }
</style>