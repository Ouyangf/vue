<template>
	<div class="search" >
		<input class="search-input" type="text" placeholder="输入城市列表名"/>
	</div>
</template>

<script>
export default {
	name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
	@import '../../../assets/style/varibles.styl'
	.search
		height: 1.82rem
		paddding: .3rem
		background: $bgColor
		.search-input
			box-sizing: border-box
			width: 100%
			height: 1.62rem
			paddding: 0 .1rem
			line-height: .62rem
			text-align: center
			border-radius: 3.06rem
			color: #666
</style>
