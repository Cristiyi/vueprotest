<template>
	<div>
		<div class="recommend-title">热销推荐</div>
		<ul>
			<li class="item border-bottom" v-for="item of recomendList" :key="item.id">
				<img class="item-img" :src="item.imgUrl">
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
				</div>
			</li>
		</ul>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'HomeRecommend',
		data () {
			return {
				recomendList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
				title: '大连圣亚海洋馆',
				desc: '浪漫大连首战，哈哈哈哈啊哈哈'
			},
			{
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
				title: '大连圣亚海洋馆',
				desc: '浪漫大连首战，哈哈哈哈啊哈哈'
			},
			{
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
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
	.item
		overflow: hidden
		display: flex
		height: 1.9rem
		.item-img
			width: 1.7rem
			height: 1.7rem
			padding: .1rem
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
			.item-button
				line-height: .44rem
				background: #ff9300
				padding: 0 .1rem
				border-radius: .06rem
				margin-top: .16rem
				color: #fff
</style>