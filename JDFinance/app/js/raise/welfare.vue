<template>
<Panel title="更多福利" :class="$style.panel">
    <section :class="$style.content">
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t7456/56/1425209238/21928/f1fe492d/599cee57Naea99020.jpg?width=250&height=330" alt="">
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t7894/126/1440046618/24763/5ce6a129/599cee04Ne77b3641.jpg?width=250&height=330" alt="">
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t6385/103/1675552688/24265/91be4150/59549aedNa30670f7.jpg?width=250&height=330" alt="">
        <em>专享福利 ></em>
    </section>
</Panel>
</template>

<script>
import Panel from '../core/panel.vue'
export default{
    components:{
        Panel,
    }

}
    
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel{
    @include panel;
    .content{
        @include flex(row);
        position: relative;
        img{
            width: 33.333%;
            height: 280px;
            display: inline-block;
        }
        em{
            display: inline-block;
            font-size: 28px;
            color: #999;
            position: absolute;
            top: -65px;
            right: 25px;
        }
    }
    
}

</style>