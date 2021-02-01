<template>
	<view style="background: #F5F8FA;">
		<myHeader style="margin-bottom: 110rpx;"></myHeader>
		<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/childrenStyletu1.png" class="childrenStyletu1"></image>
		<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/chidrenTitle1.png" class="chidrenTitle1"></image>
		<view class="multidimensionalBox">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/multidimensional.jpeg" class="multidimensional" ></image>
		</view>
		<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/childrenStyletu2.png" class="childrenStyletu2"></image>
		<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/chidrenTitle2.png" class="chidrenTitle2"></image>
		<scroll-view class="scroll-view_H" scroll-x="true"@scroll="scroll" :scroll-left="scrollLeft" >
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg1.png" class="scroll-view-item_H"></image>
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg2.png" class="scroll-view-item_H"></image>
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg3.png" class="scroll-view-item_H"></image>
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg1.png" class="scroll-view-item_H"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg2.png" class="scroll-view-item_H"></image>
		</scroll-view>
		<scroll-view class="scroll-view_H" scroll-x="true"@scroll="scroll1" :scroll-left="scrollLeft1" >
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg4.png" class="scroll-view-item_H"></image>
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg5.png" class="scroll-view-item_H"></image>
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg6.png" class="scroll-view-item_H"></image>
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg4.png" class="scroll-view-item_H"></image>
			 <image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/scrollImg5.png" class="scroll-view-item_H"></image>
		</scroll-view>
		<view class="schoolVisit_box">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/chidrenTitle3.png" class="chidrenTitle3"></image>
			<u-swiper :list="list" :effect3d="true" height=1080 effect3d-previous-margin=116 mode="none" bg-color="transparent"></u-swiper>
		</view>
		<view class="footer_box">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/downBtn.png" @click="downBtn()" class="downBtn"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/babyLand/QRcode.png" style="width: 174rpx; height: 170rpx; position: absolute;bottom: 216rpx; right: 148rpx;" ></image>
		</view>
	</view>
</template>

<script>
	import myHeader from '@/components/my_header/my_header';
	export default {
		components: { myHeader },
		data() {
			return {
				scrollLeft:0,
				scrollLeft1:100,
				scrollTop:0,
				scrollDown:0,
				list:[
					{
					image: 'https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/schoolVisit4.png',
				},
					{
						image: 'https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/schoolVisit3.png',
					},
				{
					image: 'https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/schoolVisit2.png',
				},
				]
			}
		},
		onShow() {
			console.log("关闭定时器")
			clearInterval(this.scrollTop)
			clearInterval(this.scrollDown)
			 this.scrollTop = setInterval(res=>{
				this.scrollLeft++
				if(this.scrollLeft>=this.scrollWidth*3/5){
						this.scrollLeft=0
				}
			},20)
			this.scrollDown = setInterval(res=>{
				this.scrollLeft1++
				if(this.scrollLeft1>=this.scrollWidth1*3/5+100){
						this.scrollLeft1=100
				}
			},20)
		},
		beforeCreate() {
			console.log("关闭定时器")
			clearInterval(this.scrollTop)
			clearInterval(this.scrollDown)
		},
		methods: {
			scroll: function(e) {
				// if(this.isClick){
				// 	clearInterval(this.scrollWai)
				// }
				this.scrollLeft = e.detail.scrollLeft
				this.scrollWidth = e.detail.scrollWidth
			// 	setTimeout(res=>{
			// },1000)
			},
			scroll1: function(e) {
				// if(this.isClick){
				// 	clearInterval(this.scrollWai)
				// }
				this.scrollLeft1 = e.detail.scrollLeft
				this.scrollWidth1 = e.detail.scrollWidth
			// 	setTimeout(res=>{
			// },1000)
			},
			downBtn(){
				window.location.href = "https://www.wanggougou.cn/download.html"
			}
		}
	}
</script>

<style lang="scss" scoped>
	.childrenStyletu1{
		width: 750rpx;
		height: 1160rpx;
	}
	.childrenStyletu2{
		width: 750rpx;
		height: 516rpx;
		margin-top: 36rpx;
	}
	.chidrenTitle1{
		display: block;
		width: 464rpx;
		height: 152rpx;
		margin: 60rpx auto;
	}
	.multidimensionalBox{
		height: 390rpx;
		background: #FFFFFF;
		border-radius: 20rpx;
		margin: 0 24rpx;
		padding: 16rpx;
	}
	.multidimensional{
		width: 670rpx;
		height: 358rpx;
		background: #FFFFFF;
		border-radius: 20rpx;
	}
	.chidrenTitle2{
		display: block;
		width: 336rpx;
		height: 152rpx;
		margin: 0 auto;
	}
	.schoolVisit_box{
		background-image: url("https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/schoolVisit.png");
		background-repeat: no-repeat;
		background-size: 100%;
		width: 750rpx;
		height: 1180rpx;
		padding-top: 16rpx;
	}
	.chidrenTitle3{
		display: block;
		width: 456rpx;
		height: 152rpx;
		margin: 0 auto;
		margin-bottom: 60rpx;
	}
	// 横向
	.scroll-view_H {
		white-space: nowrap;
		width: 100%;
		margin: 60rpx 0;
		
	}
	// 横向
	.scroll-view-item_H {
		display: inline-block;
		margin: 0 20rpx;
		width: 488rpx;
		height: 296rpx;
	}
	/deep/.u-list-image-wrap{
		width: 530rpx !important;
		height: 1000rpx !important;
		margin: 0 20rpx !important;
	}
	/deep/.uni-swiper-item{
	}
	
	
	.footer_box{
		background-image: url("https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/childrenFooter1.png");
		background-repeat: no-repeat;
		background-size: 100%;
		width: 750rpx;
		height: 808rpx;
		position: relative;
	}
	.downBtn{
		width: 254rpx;
		height: 70rpx;
		position: absolute;
		left: 148rpx;
		bottom: 224rpx;
	}
</style>
