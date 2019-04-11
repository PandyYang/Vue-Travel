<template>
<div>
    <div class="title">热销推荐</div>
    <ul>
        <li class="item border-bottom" v-for = "(item,index) of recommendList" :key="index">
                <img class="item-img" :src="item.imgUrl" />
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
            </div>
        </li>
    </ul>
</div>
</template>

<script>
export default {
    name: 'HomeRecommend',
    data () {
        return{
            recommendList: [{
                id: '0001',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/53/53cf6caed9f9b9ee90.img.jpg_200x200_f5476a84.jpg',
                title: '长恨歌',
                desc: '11111111111111111111111111111111'
            },{
                id: '0002',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/18/18ffcca94b1b7ca2.water.jpg_200x200_9b0d2dc4.jpg',
                title: '秦岭野生动物园',
                desc: '22222222222222222222222222222222'
            },{
                id:'0003',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/c5/a017645d82ab89f271fdfb1bd6ecc2e0.water.jpg_200x200_2de772de.jpg',
                title: '金龙峡',
                desc:'22222222222222222222222222222222222222'
            },{
                id:'0004',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1412/89/66dadfb4d982e6f88abad45a3e062342.water.jpg_200x200_0443bc40.jpg',
                title:'曲江海洋极地公园',
                desc: '44444444444444444444444444444444444444444444'
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
    .item
        overflow: hidden
        display: flex
        height: 1.9rem
        .item-img
            width: 1.7rem
            height: 1.7rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width: 0
            .item-title
                line-height: .54rem
                font-size: .34rem
                ellipsis()
            .item-desc
                line-hight: .4rem
                color: #ccc
                ellipsis()
            .item-button
                line-height: .44rem
                margin-top: .26rem
                background: #ff9300
                padding: 0 .2rem
                border-radius: .06rem
</style>