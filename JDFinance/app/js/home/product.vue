<template>
    <Panel title="新品推荐" :class="$style.panel">
        <section :class="$style.content">
            <router-link :to="{name:'home'}">
            <div :class="$style.arrow">更多尖货 ></div>
            </router-link>
            <Slider :options="options" :items="items" cname="product-slider"></Slider>
        </section>
    </Panel>

</template>

<script>
    import Panel from '../core/panel';
    import Slider from '../core/slider.vue';
    export default {
        components: {
            Panel,
            Slider
        },
        data() {
            return {
                items: [

                    {
                        href: 'home',
                        src: 'https://img12.360buyimg.com/jrpmobile/jfs/t21691/233/2361780032/59932/8cb4ce42/5b5066e3Nb460c234.jpg?width=335&height=421'
                    }, {
                        href: 'home',
                        src: 'http://img12.360buyimg.com/jrpmobile/jfs/t13021/306/1996997425/21953/bda69db3/5a2f6a17N9da099b1.jpg?width=335&height=421'
                    }, {
                        href: 'home',
                        src: 'https://img12.360buyimg.com/jrpmobile/jfs/t14125/310/1997192193/46667/3c910f8b/5a2f6a36Nad95b650.jpg?width=335&height=421'
                    }, {
                        href: 'home',
                        src: 'https://img12.360buyimg.com/jrpmobile/jfs/t15784/188/381232069/39444/8878571d/5a2f6a4aNbd5a574c.jpg?width=335&height=421'
                    }
                ],
                options:{
                    //不要指示器
                    // pagination:{
                    //     el:'.swiper-pagination',
                    //     clickable:true
                    // },
                    slidesPerView:2.3,
                    spaceBetween:30,
                    freeMode:true,
                }
            }
        }


    }
</script>

<style lang="scss"> 
.product-slider{
    .swiper-container{
        box-sizing: border-box;
        padding: 0 24px;
        .swiper-slide{
            width: 100%;
            display: inline-block;
            img{
                width: 100%;
                display: block;
                height: 314px;
                border: 1px solid #fafafa;
            }
        }
    }
}
</style>

<style lang="scss" module>
@import '../../css/element.scss';
.panel{
    @include panel;
    .content{
        padding-bottom:40px;
        position: relative;
        .arrow{
            position: absolute;
            font-size:28px;
            color:#999;
            top:-66px;
            right:20px;
        }
        
    }
}


</style>
