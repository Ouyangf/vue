<template>
	<div class="header">
		城市选择
		<router-link to="/">
		<div class="iconfont header-back">&#xe624;</div>
		</router-link>
	</div>
</template>

<script>
export default {
	name: 'City'
}
</script>

<style lang="stylus" scoped>
	@import '../../../assets/style/varibles.styl'
	.header
		position: relative
		overflow: hidden
		height: 1.86rem
		line-height: 1.86rem
		text-align: center
		color: #fff
		background: $bgColor
		font-size: 1.12rem
		.header-back
			position: absolute
			top: 0
			width: .64rem
			font-size: 1.4rem
			text-align: center
			color: #fff

</style>
