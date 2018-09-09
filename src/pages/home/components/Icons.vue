<template>
	<div class="icons">
		<swiper :options="swiperOption">
		    <swiper-slide v-for="(page, index) of pages" :key="index">
		    	<div class="icon" v-for="item of page" :key="page.id">
					<div class="icon-img">
						<img class="icon-img-content" :src="item.imgUrl">
					</div>
					<p class="icon-desc">{{item.desc}}</p>
				</div>
		    </swiper-slide>
		    <div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'HomeIcons',
		props: {
			list: Array
		},
		data () {
			return {
				swiperOption: {
					loop: true,
					pagination: '.swiper-pagination',
					autoplay: false
				}
			}
		},

		computed: {
			pages () {
				const pages = []
				this.list.forEach((item, index) => {
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
	.icons
		margin-top: .1rem
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