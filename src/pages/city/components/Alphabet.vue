<template>
	<ul class="list">
		<li class="item" v-for="(item, key) of cities" :key="key">{{key}}</li>
	</ul>
</template>

<script>
export default {
	name: 'CityAlphabet',
	props: {
		cities: Object
	}
}
</script>

<style lang="stylus" scoped>
	@import '../../../assets/style/varibles.styl'
	.list
		display: flex
		flex-direction: column
		justify-content: center
		position: absolute
		top: 3.62rem
		right: 0
		bottom: 0
		width: 1.4rem
		.item
			text-align: center
			line-height: 1.44rem
			color: $bgColor

</style>
