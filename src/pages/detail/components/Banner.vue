<template>
    <div>
        <div class="banner" @click="handleBannerClick">
            <img class="banner-img" src="https://dimg01.c-ctrip.com/images/100k0r000000h6ngg6228_C_640_320.jpg"/>
            <div class="banner-info">
                <div class="banner-tittle">大连圣亚海洋世界（AAAA景区）</div>
                <div class="banner-number">
                    <span class="iconfont banner-icon">&#xe608;</span>
                    39
                </div>
            </div>
        </div>
        <common-gallary
            :imgs="imgs"
            v-show="showGallary"
            @close="handleGallaryClose"
        ></common-gallary>
    </div>
</template>

<script>
    import CommonGallary from "common/gallary/Gallary"

    export default {
        name: "DetailBanner",
        data() {
            return {
                showGallary: false,
                imgs: [
                    'https://youimg1.c-ctrip.com/target/100s0h0000008p753ACAC_R_640_10000_Q90.jpg',
                    'https://youimg1.c-ctrip.com/target/100p0700000026ao9FE9A_R_640_10000_Q90.jpg'
                ]
            }
        },
        methods: {
            handleBannerClick() {
                this.showGallary = true
            },
            handleGallaryClose() {
                this.showGallary = false
            }
        },
        components: {
            CommonGallary
        }
    }
</script>

<style lang="stylus" scoped>
    .banner
        position relative
        overflow hidden
        height 0
        padding-bottom 55%
        .banner-img
            width 100%
        .banner-info
            display flex
            position absolute
            left 0
            right 0
            bottom 0
            line-height .6rem
            color #fff
            background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
            .banner-tittle
                flex 1
                font-size .32rem
                padding 0 .2rem
            .banner-number
                margin-top .14rem
                padding 0 .4rem
                height .32rem
                line-height .32rem
                border-radius .2rem
                background rgba(0, 0, 0, .8)
                font-size .24rem
                .banner-icon
                    font-size .24rem
</style>
