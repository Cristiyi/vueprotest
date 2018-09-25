<template>
	<div class="container" @click="handleGallaryClick">
		<div class="wrapper">
			<swiper :options="swipperOptions">
			    <swiper-slide v-for="(item,index) in imgs" :key="index">
			    	<img class="galary-img" :src="item">
			    </swiper-slide>
			    <div class="swiper-pagination" slot="pagination"></div>
	  		</swiper>
		</div>
	</div>
</template>


<script type="text/javascript">
	export default {
		name: 'CommonGallary',
		props: {
			imgs: {
				type: Array,
				default() {
					return []
				}
			}
		},
		data() {
			return {
				swipperOptions: {
					pagination: '.swiper-pagination',
					paginationType: 'fraction',
					observeParents: true,
					observer: true
				}
			}
		},
		methods: {
			handleGallaryClick() {
				this.$emit('close')
			}
		}
	}
</script>

<style lang="stylus" scoped>
	.container >>> .swipper-container
		overflow: inherit
	.container
		display: flex
		flex-direction: column
		justify-content: center
		z-index: 3
		position: fixed
		left: 0
		right: 0
		top: 0
		bottom: 0
		background: #000
		.wrapper
			height: 0
			width: 100%
			padding-bottom: 100%
			.galary-img
				width: 100%
			.swiper-pagination
				color: #fff
				bottom: -1rem
</style>