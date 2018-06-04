<template>
    <Panle title="吃喝玩乐" :class="$style.panel">
        <section :class="$style.content">
            <router-link :to="{ name: 'hone'}">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t20134/295/282544712/203452/af2cc012/5b080019Nc4fe7978.png?width=704&height=246" alt="">
            </router-link>
        </section>
    </Panle>
</template>
<script>
import Panle from '../code/panel';
export default {
    components: {
        Panle
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .content {
        img{
            display: block;
            width: 100%;
        }
    }
}
</style>
