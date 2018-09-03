<template>
	<div>
		<home-header></home-header>
		<home-swiper></home-swiper>
		<home-icons></home-icons>
	</div>
</template>

<script type="text/javascript">
	import HomeHeader from './components/Header'
	import HomeSwiper from './components/Swiper'
	import HomeIcons  from './components/Icons'
	export default {
		name: 'Home',
		components: {
			HomeHeader:HomeHeader,
			HomeSwiper:HomeSwiper,
			HomeIcons: HomeIcons
		}
	}
</script>

<style type="text/css">
</style>