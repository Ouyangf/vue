<template>
	<div>
		<div class="recommend-title">周末去哪儿</div>
		<ul>
			<li class="item" v-for="item of list">
			    <div class="item-img-wrapper">
					<img class="item-img border-bottom"  :key="item.id" :src="item.imgUrl"/>
				</div>
				<div class="item-info">
					<p class="item-titles">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
export default{
	name: 'HomeWeekend',
	props: {
		list: Array
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
		.item-img-wrapper
			height: 0
			overflow: hidden
			padding-bottom: 37.09%
			.item-img
				width: 100%
				padding: 0.4rem
		.item-info
			padding；.1rem
			.item-titles
				 line-heght: 23px
				 font-size: .32rem
				 ellipsis()
			.item-desc
				line-height: 1.4rem
				color: #ccc
				ellipsis()
</style>

