<template>
	<div>
		<div class="recommend-title">周末去哪</div>
		<ul>
			<li class="item border-bottom" v-for="item of list" :key="item.id">
				<div><img class="item-img" :src="item.imgUrl"></div>
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>
			</li>
		</ul>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'HomeWeekend',
		props: {
			list: Array
		},
		
	}
</script>

<style type="text/css" lang="stylus" scoped>
	
	.recommend-title
		margin-top: .2rem
		line-height: .8rem
		background: #eee
		text-indent: .2rem
	.item-img-wrapper
		overflow: hidden
		height: 0
		padding-bottom: 33.9%
	.item-img
		width: 100%
	.item-info  
		flex: 1
		padding: .1rem
		min-width: 0
		.item-title
			line-height: .54rem
			font-size: .32rem
		.item-desc
			line-height: .4rem
			color: #ccc
</style>