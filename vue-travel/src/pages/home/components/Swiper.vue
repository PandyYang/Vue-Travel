<template>
    <div class="wrapper">
        <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img 
                class="swiper-img"
                :src="item.imgUrl"
            />
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default{
    name: 'HomeSwiper',
    data () {
        return{
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList:[{
                id: '0001',
                imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/fe/ca8ed7adc3ff9f02.jpg_750x200_49735140.jpg'
            },{
                id: '0002',
                imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/ed5f4115226306e48e6fad106a038afe.jpg_750x200_64df48d6.jpg'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff !important
    .wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 31.25%
        background: #eee
        .swiper-img
            width: 100%
</style>
