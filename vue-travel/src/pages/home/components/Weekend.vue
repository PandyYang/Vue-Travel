<template>
<div>
    <div class="title">周末去哪儿</div>
    <ul>
        <li class="item border-bottom" v-for = "(item,index) of recommendList" :key="index">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl" />
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
    </ul>
</div>
</template>

<script>
export default {
    name: 'HomeWeekend',
    data () {
        return{
            recommendList: [{
                id: '0001',
                imgUrl: 'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
                title: '长恨歌',
                desc: '11111111111111111111111111111111'
            },{
                id: '0002',
                imgUrl: 'http://img1.qunarzz.com/sight/source/1811/63/808c022b285a2c.jpg_r_640x214_ad984479.jpg',
                title: '秦岭野生动物园',
                desc: '22222222222222222222222222222222'
            },{
                id:'0003',
                imgUrl: 'http://img1.qunarzz.com/sight/source/1505/30/67d5e62ca78a29.jpg_r_640x214_9dfb4295.jpg',
                title: '金龙峡',
                desc:'333333333333333333333333333333333'
            },{
                id:'0004',
                imgUrl: 'http://img1.qunarzz.com/sight/source/1507/de/e6ba44d61894c0.jpg_r_640x214_847324d0.jpg',
                title:'曲江海洋极地公园',
                desc: '44444444444444444444444444444444'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/minins.styl'
    .title
        line-height: .8rem
        background: #eee
        text-indent: .2rem
    .item-img-wrapepr
        overflow: hidden
        height: 0
        padding-bottom: 33.9%
    .item-img
        width: 100%
    .item-info
        padding: .1rem
        .item-title
            line-height: .54rem
            font-size: .34rem
            ellipsis()
        .item-desc
            line-hight: .4rem
            color: #ccc
            ellipsis()
</style>