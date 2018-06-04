<template>
    <Panel title="新手特权" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.item">
                <h4>下载APP<span :class="$style.red">送888元礼包</span></h4>
                <p :class="$style.gray">新手专享</p>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t21559/102/59104594/47942/f8d9e459/5af9055dN55aa9554.jpg?width=335&height=421" alt="">
            </div>
            <div :class="$style.item">
                <ul>
                    <li>
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t21559/102/59104594/47942/f8d9e459/5af9055dN55aa9554.jpg?width=335&height=421" alt="">
                        <h4 :class="$style.red">领取128元新手礼包</h4>
                        <p :class="$style.gray">立即开通</p>
                    </li>
                    <li>
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t21559/102/59104594/47942/f8d9e459/5af9055dN55aa9554.jpg?width=335&height=421" alt="">
                        <h4 :class="$style.red">打白条</h4>
                        <p :class="$style.gray">立即开通享豪礼</p>
                    </li>
                </ul>
            </div>
        </section>
    </Panel>   
</template>

<script>
import Panel from '../code/panel'
export default {
    components: {
        Panel
    }
}
</script>

<style lang="scss" module>
    @import '../../css/element.scss';
    .panel{
        @include panel;
        >h4{
            border-bottom: 1px solid #ddd;
        }
        .content{
            @include list(row);
            .item{
                width: 50%;
                box-sizing: border-box;
                &:first-child{
                    padding: 32px 20px;
                    text-align: center;
                    border-right: 1px solid #ddd;
                    img{
                        height: 144px;
                    }

                }
                h4{
                    font-size: 26px;
                    line-height: 40px;
                }
                .red{
                    color: #f00
                }
                .gray{
                    color: #999;
                    font-size: 24px;
                }
                p{  
                    margin-top: 6px;
                    font-size: 24px
                }
                ul{
                    width: 100%;
                    li{
                        height: 144px;
                        padding: 32px 20px;
                        box-sizing: border-box;
                        &:first-child{
                            border-bottom: 1px solid #ddd;
                        }
                        h4{
                            white-space: nowrap;
                            text-overflow: ellipsis;
                            overflow: hidden;

                        }
                        img{
                            width: 80px;
                            height: 80px;
                            float: right;
                        }
                    }
                }
            }
        }

    }
</style>
