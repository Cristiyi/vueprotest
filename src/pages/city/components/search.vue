<template>
	<div class="search">
		<input class="search-input" type="text" placeholder="输入城市名或拼音"></input>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'CitySearch'
	}
</script>

<style type="text/css" lang="stylus" scoped> 
	.search
		height: .72rem
		background: #00bcd4
		padding: 0 .1rem
		.search-input
			box-sizing: border-box
			width: 100%
			height: .62rem
			line-height: .62rem
			text-align: center
			border-radius: .06rem
			color: #666
			padding: 0 .1rem
</style>