<template>
	<div>
		<div class="banner" @click="handleBannerClick">
			<img class="banner-img" :src="bannerImg">
			<div class="banner-info">
				<div class="banner-tittle">{{this.sightName}}</div>
				<div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span>{{this.gallaryImgs.length}}</div>
			</div>
		</div>
		<fade>
			<common-gallary :imgs="imgs" v-show="showGalary" @close="handleGallaryClose"></common-gallary>
		</fade>
	</div>
</template>	

<script type="text/javascript">
	import CommonGallary from 'common/gallary/Gallary'
	import Fade from 'common/fade/Fade'
	export default {
		name: 'DetailBanner',
		props: {
			sightName: String,
			bannerImg: String,
			gallaryImgs: Array
		},
		components: {
			CommonGallary,
			Fade
		},
		data() {
			return {
				showGalary: false,
				imgs: ["http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_800x800_70debc93.jpg", "http://img1.qunarzz.com/sight/p0/1709/76/7691528bc7d7ad3ca3.img.png_800x800_9ef05ee7.png"]
			}
		},
		methods: {
			handleBannerClick() {
				this.showGalary = true
			},
			handleGallaryClose() {
				this.showGalary = false
			}
		}
	}
</script>

<style type="text/css" lang="stylus" scoped>
	.banner
		position: relative
		overflow: hidden
		height: 0
		padding-bottom: 55%
		.banner-img
			width: 100%
		.banner-info
			display: flex
			position: absolute
			left: 0
			right: 0
			bottom: 0
			line-height: .6rem
			color: #fff
			background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
			.banner-tittle
				flex: 1
				font-size: .32rem
				padding: 0 .2rem
			.banner-number
				margin-top: .14rem
				padding: 0 .4rem
				line-height: .32rem
				height: .32rem
				border-radius: .2rem
				background: rgba(0, 0, 0, 0.8)
				font-size: .24rem
				.banner-icon
					font-size: .24rem
</style>