<template>
  	<div class="wrapper">
  		<swiper :options="swiperOption" v-if="showSwiper">
	    <!-- slides -->
	    <swiper-slide v-for="item of list" :key="item.id">
	    	<img class="swiper-img" :src="item.imgUrl">
	    </swiper-slide>
	    <!-- Optional controls -->
	  </swiper>
  	</div>
</template>


<script>
  export default {
    name: 'HomeSwoper',
    props: {
      list: Array
    },
    data () {
      return {
        swiperOption: {
          // some swiper options/callbacks
         loop: true
          // ...
        }
      }
    },
    computed: {
      showSwiper() {
        return this.list.length
      }
    }
  }
</script>

<style type="text/css" lang="stylus" scoped>

    .wrapper >>> .swiper-pagination-bullet-active
    	background: #fff

	.wrapper
		witdh: 100%
		height: 0
		overflow: hidden
		padding-bottom: 31.25%
		background: #eee
		.swiper-img
			width: 100%;

</style>