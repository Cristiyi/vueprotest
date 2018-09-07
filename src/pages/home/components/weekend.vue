<template>
	<div>
		<div class="recommend-title">周末去哪</div>
		<ul>
			<li class="item border-bottom" v-for="item of recomendList" :key="item.id">
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
		data () {
			return {
				recomendList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
				title: '大连圣亚海洋馆',
				desc: '浪漫大连首战，哈哈哈哈啊哈哈'
			},
			{
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
				title: '大连圣亚海洋馆',
				desc: '浪漫大连首战，哈哈哈哈啊哈哈'
			},
			{
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
				title: '大连圣亚海洋馆',
				desc: '浪漫大连首战，哈哈哈哈啊哈哈'
			}
			]}
		}
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