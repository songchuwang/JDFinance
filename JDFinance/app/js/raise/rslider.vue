<template>
    <Panel title="金融头条" :class="$style.panel">
        <section :class="$style.content">
            <swiper :options="options">
                <swiper-slide :class="$style.item" v-for="item in items" :key="item.text">
                    {{item.text}} <em>> </em>         
                </swiper-slide>
            </swiper>
        </section>
    </Panel>
</template>

<script>
    import {
        swiper,
        swiperSlide
    } from 'vue-awesome-swiper'
    import Panel from '../core/panel.vue'
    export default {
        components: {
            Panel,
            swiper,
            swiperSlide
        },
        data() {
            return {
                options: {
                    autoplay: true,
                    loop: true,
                    direction: 'vertical',

                },
                items: [{
                        text: '签到领流量，1元500M！'
                    },
                    {
                        text: '百万白条券免费送，速来领取！！ '
                    }

                ]
            }
        }

    }
</script>
<style lang="scss">
.swiper-container-vertical{
    height: 72px;
    .swiper-slide{
        font-family: PingFangSC-Medium;
        font-size: 28px;
        color: #333;
        em{
            float: right;
            margin-right: 20px;
            color: #ddd;
        }
    }

}

</style>


<style lang="scss" module>
    @import '../../css/element.scss';
    .panel {
        @include panel;
        margin-top: 120px !important;       
        >h4 {
            display: none;
        }
        .content {  
            height: 72px;
            line-height: 72px;
            text-align: left;
            text-overflow: ellipsis;
            overflow: hidden;
            padding-left: 170px;
            background:url(http://m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png) left center no-repeat;
       
        }
    }
</style>