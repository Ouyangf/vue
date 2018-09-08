<template>
	<div>
		<div class="recommend-title">热销推荐</div>
		<ul>
			<li class="item" v-for="item of recommendList">
					<img class="item-img border-bottom"  :key="item.id" :src="item.imgUrl"/>
				<div class="item-info">
					<p class="item-titles">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
export default{
	name: 'HomeRecommend',
	data () {
		return {
			recommendList: [{
			id: '0001',
			imgUrl: 'https://imgs.qunarzz.com/vc/a9/04/30/2aefd5c3218d1ba5edd9e51d06.jpg_92.jpg',
			title: '浪漫大连首站，浪漫的海洋主题乐园',
			desc: '大连圣亚海洋世界' 
			},{
			id: '0001',
			imgUrl: 'https://imgs.qunarzz.com/vc/a9/04/30/2aefd5c3218d1ba5edd9e51d06.jpg_92.jpg',
			title: '浪漫大连首站，浪漫的海洋主题乐园',
			desc: '大连圣亚海洋世界' 
			},{
			id: '0001',
			imgUrl: 'https://imgs.qunarzz.com/vc/a9/04/30/2aefd5c3218d1ba5edd9e51d06.jpg_92.jpg',
			title: '浪漫大连首站，浪漫的海洋主题乐园',
			desc: '大连圣亚海洋世界' 
			},{
			id: '0001',
			imgUrl: 'https://imgs.qunarzz.com/vc/a9/04/30/2aefd5c3218d1ba5edd9e51d06.jpg_92.jpg',
			title: '浪漫大连首站，浪漫的海洋主题乐园',
			desc: '大连圣亚海洋世界' 
			}]
		}		
	}
}
</script>

<style lang="stylus" scoped>
@import '../../../assets/style/mixins.styl'
	.recommend-title
		margin-top: .1rem 
		line-height: 2.8rem
		background: #eee
		text-indent: 2.2rem
	.item
		overflow:hidden
		display: flex
		height: 4.9rem
		width: 100%
		.item-img
			height: 83%
			padding: 0.4rem
		.item-info
			flex: 1
			padding；.1rem
			.item-titles
				 line-heght: 23px
				 font-size: .32rem
				 ellipsis()
			.item-desc
				line-height: 1.4rem
				color: #ccc
				ellipsis()
			.item-button
				line-height: 28px
				background: #ff9300
				padding: 0 .2rem
				color: #fff
				border-radius: .46rem
				border: 1px solid #ccc
</style>
