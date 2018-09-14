<template>
	<div class="header">
		<div class="header-left">
			<div class="iconfont back-icon">&#xe624;</div>	
		</div>
		<div class="header-input"><span class="iconfont">&#xe632;</span>输入城市经典游玩主题</div>
		<router-link to="/city">
			<div class="header-right">
			<!-- {{this.$store.state.city}} -->
			{{this.city}}
			<span class="arrow-iconfont arrow-icon">&#xe624;</span>
		</div>
		</router-link>
	</div>
</template>

<script type="text/javascript">
	import { mapState,mapGetters } from 'vuex'
	export default {
		name: 'Home',
		computed: {
			...mapState(['city']),
			...mapGetters(['doubleCity'])
		}
	}
</script>

<style type="text/css" lang="stylus" scoped>

	/*@import '../../../assets/styles/varibles.styl'*/
	.header
		display: flex
		height: .86rem
		line-height: .86rem
		background: #00bcd4
		color: #fff
		.header-left
			width: .64rem
			float: left
			.back-icon
				text-align: center
				font-size: .4rem
		.header-input
			flex: 1
			margin-top: .12rem
			height: .64rem
			line-height: .64rem
			margin-left .2rem
			padding-left: .2rem
			background:#fff
			border-radius: .1rem
			color: #ccc
		.header-right
			min-width: 1.04rem
			padding: 0 .1rem
			float: right
			text-align: center
			color: white
			.arrow-icon
				font-size: .24rem
				margin-left: .14rem


</style>