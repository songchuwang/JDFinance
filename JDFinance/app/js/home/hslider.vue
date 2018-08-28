<template>
    <article class="">
        <Slider :items="items" :cname="$style.slider"></Slider>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key='item.img'>
                <router-link :to="{name:item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
    import Slider from '../core/slider.vue'
    export default {
        components: {
            Slider
        },
        data() {
            return {
                items: [{
                    href: 'home',
                    src: 'https://img12.360buyimg.com/jrpmobile/jfs/t23089/172/1880749724/39100/b0c96e6d/5b6d73b2N8835f3e6.jpg?width=750&height=320'

                }, {
                    href: 'home',
                    src: 'https://img12.360buyimg.com/jrpmobile/jfs/t23773/98/1923793411/42617/896ed155/5b6d73a9N15430d1e.jpg?width=750&height=320'
                }, {
                    href: 'home',
                    src: 'https://img12.360buyimg.com/jrpmobile/jfs/t24883/191/374540257/28467/dcd73445/5b6d73b6N21bda9be.jpg?width=750&height=320'
                }, {
                    href: 'home',
                    src: 'https://img12.360buyimg.com/jrpmobile/jfs/t23773/98/1923793411/42617/896ed155/5b6d73a9N15430d1e.jpg?width=750&height=320'
                }],
                enters: [{
                    href: 'download',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
                    title: '优惠券'
                }, {
                    href: 'home',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
                    title: '领福利'
                }, {
                    href: 'home',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
                    title: '抢钢镚'
                }, {
                    href: 'home',
                    img: 'https://img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
                    title: '白条提额'
                }]
            }


        }

    }
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.slider{
    margin-top: 120px;
    img{
        width: 100%;
    }
}
.list{
    @include list(row);
    background: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    a{
        text-decoration: none;
    }
    .item{
        text-align: center;
        img{
            display: inline-block;
            width: 90px;
            height: 90px;
        }
        h4{
            font-size: 26px;
            margin-top: 12px;
            color: #666; 
        }

    }
}


</style>
