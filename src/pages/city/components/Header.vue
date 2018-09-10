<template>
	<div class="header">
		城市选择
		<router-link to="/">
			<div class="iconfont header-back">&#xe624;</div>
		</router-link>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'CityHeader'
	}
</script>

<style type="text/css" lang="stylus" scoped> 
	.header
		overflow: hidden
		height: .86rem
		line-height: .86rem
		background: #00bcd4
		color: #fff
		text-align: center
		font-size: .32rem
		position: relative
		.header-back
			color: white
			position: absolute
			top: 0
			left: 0
			width: .64rem
			text-align: center
			font-size: .4rem
</style>