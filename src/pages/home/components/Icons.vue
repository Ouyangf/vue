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
    data () {
        return {
            iconList: [{
                id:'0001',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
                desc:'景点门票'
            },{
                id:'0002',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1711/df/86cbcfc533330d02.png',
                desc:'滑雪季'
            },{
                id:'0003',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1710/a6/83f636bd75ae6302.png',
                desc:'泡温泉'
            },{
                id:'0004',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1611/35/2640cab202c41b02.png',
                desc:'动植园'
            },{
                id:'0005',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
                desc:'景点门票'
            },{
                id:'0006',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1711/df/86cbcfc533330d02.png',
                desc:'滑雪季'
            },{
                id:'0007',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1710/a6/83f636bd75ae6302.png',
                desc:'泡温泉'
            },{
                id:'0008',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1611/35/2640cab202c41b02.png',
                desc:'动植园'
            },{
                id:'0009',
                imgUrl:'https://img1.qunarzz.com/piao/fusion/1611/a9/ffc620dbda9b9c02.png',
                desc:'景点门票'
            }]
        }
    },
    computed: {
        pages () {
            const pages = []
            this.iconList.forEach((item,index)=>{
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
            line-height: 10.44rem
            color: $darkTextColor
            text-align:center
                              
</style>
