<template>
    <div class="icons">
        <div class="icon" v-for="item of iconList" :key="item.id">
            <div class="icon-img">
                <img class="icon-img-content" :src="item.url">
            </div>
            <p class="icon-desc">{{item.desc}}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "HomeIcons",
        data() {
            return {
                iconList: [{
                    id: '001',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-04.png',
                    desc: '景点'
                }, {
                    id: '002',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-03.png',
                    desc: '地点'
                }, {
                    id: '003',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-03.png',
                    desc: '地点'
                }, {
                    id: '004',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-03.png',
                    desc: '地点'
                }, {
                    id: '005',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-03.png',
                    desc: '地点'
                }, {
                    id: '006',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-03.png',
                    desc: '地点'
                }, {
                    id: '007',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-03.png',
                    desc: '地点'
                }, {
                    id: '008',
                    url: '//pic.c-ctrip.com/platform/h5/home/pic-tmh-03.png',
                    desc: '地点'
                }]
            }
        }
    }
</script>

<style lang="stylus" scoped>
    @import "~styles/varibles.styl"
    .icons
        overflow hidden
        height 0
        padding-bottom 50%
        .icon
            position relative
            overflow hidden
            float left
            width 25%
            height 0
            padding-bottom 25%
            .icon-img
                position absolute
                top 0
                left 0
                right 0
                bottom .44rem
                box-sizing border-box
                padding .1rem
                .icon-img-content
                    display block
                    margin 0 auto
                    width 100%
            .icon-desc
                position absolute
                left 0
                right 0
                bottom 0
                height .44rem
                line-height .44rem
                text-align center
                color $darkTextColor
</style>
