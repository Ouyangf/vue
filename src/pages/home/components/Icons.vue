<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page,index) of pages" :key="index">
                <div class="icon" v-for="item of page" :key="item.id">                         
                        <div class="icon-img">
                            <img class="icon-img-content" :src="item.imgUrl"/>
                        </div>
                        <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
         </swiper>
    </div>
</template>
<script>
export default{
    name: 'HomeIcons',
    props: {
        list: Array
    },
    computed: {
        pages () {
            const pages = []
            this.list.forEach((item,index)=>{
                const page = Math.floor(index / 8)
                if (!pages[page]) {
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>
<style lang="stylus" scoped>
    @import '../../../assets/style/varibles.styl'
    @import '../../../assets/style/mixins.styl'
    .icons >>> .swiper-container
        //overflow: hidden
        height: 0
        padding-bottom: 50%
       // background: green
    .icon
        position: relative
        overflow: hidden
        float: left
        height: 0
        width: 25%
        padding-bottom: 25%
      //  background: red
        .icon-img
            position: absolute
            top: 0
            left: 0
            right: 0
            bottom: 1.44rem
         //   background: blue
            .icon-img-content
                height: 100%
                text-align: center
                margin: 0 auto
                display: block
        .icon-desc
            position:absolute
            left: 0
            right: 0
            height: .44rem
            line-height: 10rem
            color: $darkTextColor
            text-align:center
            ellipsis()
                              
</style>
