<template>
<div class="wrapper">
     <swiper :options="swiperOption" >
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default{
    name:'HomeSwiper',
    data () {
        return {
            swiperOption:{
                pagination:'.swiper-pagination',
                loop:true
            },
            swiperList:[{
                id:'0001',
                imgUrl:'https://z1.muscache.cn/im/pictures/9b0ae17d-7cfe-41bb-9a89-f38287f92c3a.jpg?aki_policy=large'
            },
            {
                id:'0002',
                imgUrl:'https://z1.muscache.cn/im/pictures/e772f521-30e7-4513-b1d4-449cfc688a13.jpg?aki_policy=large'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped> 
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff !important
    .wrapper
        width: 100%
        height: 0
        padding-bottom: 67%
        background: #eee
        .swiper-img
            width: 100%
</style>
