<template>
  <div class="wraaper">
	  <swiper :options="swiperOption">
	    <!-- slides -->
	    <swiper-slide v-for="item of swiperList" :key="item.id">
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
		data: function() {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true
				},
				swiperList: [{
					id: '0001',
					imgUrl: "https://source.qunarzz.com/site/images/wns/2019505_dujia_homepage_top_banner_5.jpg"
				}, {
					id: '0002',
					imgUrl: "https://source.qunarzz.com/site/images/wns/20190530_qunar_dujia_homepage_top_banner_1.jpg"
				}, {
					id: '0003',
					imgUrl: "https://source.qunarzz.com/site/images/wns/20190531_dujia_homepage_top_banner_4.jpg"
				}]
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