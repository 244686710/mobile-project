<template>
    <div :class="$style.header">
         <span :class="$style.left">
             <em>注册</em>&nbsp;|&nbsp;<em>登陆</em>
         </span>
         <btn :class="$style.btnDownload">App下载</btn>
    </div>
</template>

<script>
import Btn from '../code/btn'

export default {
    components: {
        Btn
    },
    data () {
        return {

        }
    }

}
</script>

<style lang="scss" module>
@import '../../css/px2rem.scss';
    .header{
        color: #666;
        height: 100px;
        line-height: 100px;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;

        font-size: 32px;
        background: #fff ;
        background-size: auto 50%;
        z-index: 100;
        .left {
            font-size: 28px;
            height: px2rem(30);
            margin: 17px 0 0 18px;
        }
        .btnDownload{
            float: right;
            font-size: 24px;
            border-width: 0;
            height: 56px;
            line-height: 56px;
            min-width: 120px;
            padding: 0;
            border-radius: 4px;
            margin: 24px 24px 0 0
        }

    }
</style>
