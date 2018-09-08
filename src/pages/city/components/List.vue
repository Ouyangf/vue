<template>
	<div class="list" >
		<div class="area">
			<div class="title border-topbottom">当前城市</div>
			<div class="button-list">
				<div class="button-wrapper">
					<div class="button">
						北京
					</div>				
				</div>
			</div>
		</div>
		<div class="area">
			<div class="title border-topbottom">热门城市</div>
			<div class="button-list">
				<div class="button-wrapper">
					<div class="button">
						北京
					</div>				
				</div>
				<div class="button-wrapper">
					<div class="button">
						北京
					</div>				
				</div>
				<div class="button-wrapper">
					<div class="button">
						北京
					</div>				
				</div>
				<div class="button-wrapper">
					<div class="button">
						北京
					</div>				
				</div>
			</div>
		</div>
		<div class="area">
			<div class="title border-topbottom">A</div>
			<div class="item-list">
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
			</div>
			<div class="title border-topbottom">A</div>
			<div class="item-list">
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
			</div>
			<div class="title border-topbottom">A</div>
			<div class="item-list">
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
				<div class="item border-bottom">阿尔拉</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CityList'
}
</script>

<style lang="stylus" scoped>
	@import '../../../assets/style/varibles.styl'
	.border-topbottom
		&:before
			border-color: #ccc
		&:after
			border-color: #ccc
	.border-bottom
		&:before
			border-color: #ccc
	.list
		overflow: hidden
		position: absolute
		top: 3.6rem
		left: 0
		right: 0
		bottom: 0
		.title
			line-height: 1.4rem
			background: #eee
			padding-left: .2rem
			color: #666
		.button-list
			overflow: hidden
			padding: 0.16rem 33px 2px 6px
			.button-wrapper
				float: left
				width: 33.33%
				.button 
					padding: 2px 0
					text-align: center
					margin: .5rem
					border: 1px solid #ccc
					border-radius: .36rem
		.item-list
			.item
				line-height: 1.76rem
				color: #666
				padding-left: 0.8rem
</style>

