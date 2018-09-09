<template>
	<div class="list" ref="wrapper">
		<div>
			<div class="area">
				<div class="title border-topbottom">当前城市</div>
				<div class="button-list">
					<div class="button-wrapper">
						<div class="button">
							{{this.$store.state.city}}
						</div>				
					</div>
				</div>
			</div>
			<div class="area">
				<div class="title border-topbottom">热门城市</div>
				<div class="button-list">
					<div 
					class="button-wrapper" 
					v-for="item of hot" 
					:key="item.id"
					@click="handleCityClick(item.name)">
						<div class="button">
							{{item.name}}
						</div>				
					</div>
				</div>
			</div>
			<div 
				class="area" 
				v-for="(item,key) of cities" 
				:key="key"
				:ref="key">
				<div class="title border-topbottom">{{key}}</div>
				<div 
				class="item-list" 
				v-for="innerItem of item" 
				:key="innerItem.id"
				@click="handleCityClick(innerItem.name)">
					<div class="item border-bottom" >{{innerItem.name}}</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
	name: 'CityList',
	props: {
		hot: Array,
		cities: Object,
		letter: String
	},
	methods: {
		handleCityClick (city) {
			this.$store.dispatch('changeCity',city)
		}
	},
	mounted () {
		this.scroll = new Bscroll(this.$refs.wrapper);
	},
	watch: {
		letter () {
			if (this.letter) {
				const element = this.$refs[this.letter][0]
				this.scroll.scrollToElement(element)
			}
		}
	}
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
				color: black
				padding-left: 0.8rem
</style>

