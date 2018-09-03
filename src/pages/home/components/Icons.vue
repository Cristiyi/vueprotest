<template>
	<div class="icons">
		<swiper>
		    <swiper-slide v-for="(page, index) of pages" :key="index">
		    	<div class="icon" v-for="item of page" :key="page.id">
					<div class="icon-img">
						<img class="icon-img-content" :src="item.imgUrl">
					</div>
					<p class="icon-desc">{{item.desc}}</p>
				</div>
		    </swiper-slide>
	  </swiper>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'HomeIcons',
		data () {
			return {
				iconList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '景点门票'
				}, {
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '泡温泉'
				}, {
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '大粉不'
				},
				{
					id: '0004',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '大歪不'
				},
				{
					id: '0005',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '小歪不'
				},
				{
					id: '0006',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '小心心'
				},
				{
					id: '0007',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '小熊熊'
				},{
					id: '0008',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '小不不'
				},{
					id: '0009',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '小阿不'
				}]
			}
		},

		computed: {
			pages () {
				const pages = []
				this.iconList.forEach((item, index) => {
					const page = Math.floor(index / 8)
					if(!pages[page]) {
						pages[page] = []
					}
					pages[page].push(item)
				})
				return pages
			}
		}

	}	
</script>

<style type="text/css" lang="stylus">
	.icons >>> .swiper-container
		height: 0
		padding-bottom: 50%
	.icon
		position: relative
		float: left
		width: 25%
		padding-bottom: 25%
		height: 0
		overflow: hidden
		.icon-img
			position: absolute
			top: 0
			left: 0
			right: 0
			bottom: .44rem
			box-sizing: border-box
			padding: .1rem
			.icon-img-content
				display: block
				margin: 0 auto
				height: 100%
		.icon-desc
			position: absolute
			left: 0
			right: 0
			bottom: 0
			height: .44rem
			line-height: .44rem
			color: #333
			text-align: center
			overflow: hidden
			white-space: nowrap
			text-overflow: ellipsis


</style>