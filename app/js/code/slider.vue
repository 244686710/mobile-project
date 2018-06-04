<template>
    <section :class="cname">
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{name: item.href}">
                    <img :src="item.src" alt="">
                </router-link>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination" v-if="options.pagination"/>
        </swiper>
    </section>
</template>
<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
    components: {
        swiper,
        swiperSlide
    },
    props: {
        cname: String,
        options: {
            type: Object,
            default () {
                return {
                    autoplay: true,
                    loop: true,
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true
                    },
                    notNextTick: false
                }
            }
        },
        items: {
            type: Array,
            default () {
                return [{href: '', src: ''}]
            }
        }
    }

}
</script>
<style lang="css">
@import '../../css/swiper-4.2.6.min.css';
</style>

