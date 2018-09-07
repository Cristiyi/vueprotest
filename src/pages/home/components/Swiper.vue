<template>
  	<div class="wrapper">
  		<swiper :options="swiperOption">
	    <!-- slides -->
	    <swiper-slide v-for="item of swiperList" :key="item.id">
	    	<img class="swiper-img" :src="item.imgUrl">
	    </swiper-slide>
	    <!-- Optional controls -->
	  </swiper>
  	</div>
</template>


<script>
  export default {
    name: 'HomeSwoper',
    data () {
      return {
        swiperOption: {
          // some swiper options/callbacks
         loop: true
          // ...
        },
        swiperList: [{
        	id: '0001',
        	imgUrl: 'https://img1.qunarzz.com/travel/poi/1808/f9/47b66071eceb4d37.jpg'
        }, {
        	id: '0002',
        	imgUrl: 'https://img1.qunarzz.com/p/tts5/201304/18/902c99577281d75593835fbb.jpg_r_640x420x90_e9e398c8.jpg'
        }]
      }
    },
  }
</script>

<style type="text/css" lang="stylus" scoped>

    .wrapper >>> .swiper-pagination-bullet-active
    	background: #fff

	.wrapper
		witdh: 100%
		height: 0
		overflow: hidden
		padding-bottom: 66%
		background: #eee
		.swiper-img
			width: 100%;

</style>