<template>
    <div>
        <Slider :items="items" :cname="$style.slider"/>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{name: item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{item.title}}</h4>
                </router-link>
            </div>
        </section>
    </div>
</template>

<script>
import Slider from '../code/slider'
export default {
    components: {
        Slider
    },
    data () {
        return {
            items: [{
                href: 'home',
                src: 'https://img12.360buyimg.com/jrpmobile/jfs/t20230/362/280260297/33558/9ade24ef/5b07fe15Nc753456b.jpg?width=750&height=320',
            },{
                href: 'home',
                src: 'https://img12.360buyimg.com/jrpmobile/jfs/t20305/116/273290562/49600/f6486521/5b07febaN2cc4e8b8.jpg?width=750&height=320',
            }
            ],
            enters: [{
                img: '//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
                href: 'home',
                title: '优惠券'
            },{
                img: '//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
                href: 'home',
                title: '领红包'
            },{
                img: '//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
                href: 'home',
                title: '抢钢镚'
            },{
                img: '//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
                href: 'home',
                title: '领白条'
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
            width: 100%
        }
    }
    .list {
        @include list(row);
        background: #fff;
        padding-top: 40px;
        padding-bottom: 20px;
        justify-content: space-around;
        a{
            text-decoration: none;
        }
        .item {
            text-align: center;
            img{
                display: inline-block;
                width: 90px;
                height: 90px;
            }
            h4{
                font-size: 26px;
                margin-top: 12px;
            }
        }
    }
</style>
