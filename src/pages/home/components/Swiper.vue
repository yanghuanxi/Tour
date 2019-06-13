<template>
  <div class="wraaper">
	  <swiper :options="swiperOption" v-if="showSwiper">
	    <!-- slides -->
	    <swiper-slide v-for="item of list" :key="item.id">
	    	<img class="swiper-img" :src="item.imgUrl" />
	    </swiper-slide>
	    <!-- Optional controls -->
	    <div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
  </div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		props: {
		  list: Array
		},
		data: function() {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true
				},
			}
		},
		computed: {
			showSwiper () {
				return this.list.length
			}
		}
	}
</script>
<style lang="stylus" scoped>
	.wraaper >>> .swiper-pagination-bullet-active
	  background: #fff
	.wraaper
	  overflow: hidden
	  width: 100%
	  height: 0
	  padding-bottom: 25.6%
	  background: #eee
	  .swiper-img
	     width: 100%
</style>