<template>
	<view>
		<myHeader style="margin-bottom: 100rpx;"></myHeader>
		<view class="wrap">
			<view class="wrap_box1">
				<swiper class="headPicture" :indicator-dots="false" autoplay="true" indicator-color="rgba(255, 255, 255, .3)" indicator-active-color="#FFFFFF" interval="2000" duration="500" circular="true" >
				    <swiper-item v-for="(item, index) of swiperImg" :key="" @click="goDelia(index)" >
				       <image :src="item.image" class="headPicture" ></image>
				    </swiper-item>
				</swiper>
				<view class="">
				</view>
			</view>
				<view class="title1">
					
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/title1.png" class="title1Img"></image>
					<view class="title1_text">
						旺狗狗是一个源于父母对孩子全方位实时呵护而开发的APP，以宝贝安全为核心，运用AI技术，专注打造
						3-6岁儿童感兴趣的学习场景，以寓教于乐的方式，培养儿童自发学习力，激发儿童思维；
						通过定制家庭教育百科，全面培养儿童素质，让亲子共同成长；以大数据链接名校资源，帮助家长改善儿童学习环境，从基础教育开始，开启美好人生。
						旺狗狗，无形的纽带，妈妈的爱！
					</view>
				</view>
				<view class="pagesImg-box">
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/safe.png" class="pagesImg" v-show="pageImgIndex==0"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/game.png" class="pagesImg" v-show="pageImgIndex==1"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/pc20201212/product/family/fa.png" class="pagesImg" v-show="pageImgIndex==2"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/school1.jpg" class="pagesImg" v-show="pageImgIndex==3"></image>
				</view>
				<view class="pages">
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/clickSafe.png" class="pageImg" v-if="pageImgIndex==0"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/unclickSafe.png" class="pageImg" v-else @click="pageImgIndex=0"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/clickGame.png" class="pageImg" v-if="pageImgIndex==1"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/unclickGame.png" class="pageImg" v-else @click="pageImgIndex=1"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/clickHome.png" class="pageImg" v-if="pageImgIndex==2"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/unclickHome.png" class="pageImg" v-else @click="pageImgIndex=2"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/clickSchool.png" class="pageImg" v-if="pageImgIndex==3"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/unclickSchool.png" class="pageImg" v-else @click="pageImgIndex=3"></image>
				</view>
				<view class="title1">
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/title2.png" class="title2Img"></image>
					<view class="vice-title">
						家庭端、校园端双覆盖
					</view>
					<view class="title2_text" style="text-align: center;">
						旺狗狗科技，采用大数据分析驱动，AI交互技术，覆盖家庭、校园多个场景，宝贝乐园帮助孩子自主学习，家庭学院精选各类育儿知识，让亲子家庭共同成长；宝贝安全链接智能安全设备，支持校园考勤、多重实时定位，校内校外全方位守护；幼园风采优选名校，方便筛选理想学校。
					</view>
				</view>
				<view class="exhibition_box">
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/familySide.png" class="exhibitionImg"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/campusEnd1.png" class="exhibitionImg"></image>
				</view>
		</view>
		
	</view>
</template>

<script>
	import myHeader from '@/components/my_header/my_header';
	export default {
		data() {
			return {
				height: "",
				pageImgIndex:0,
				swiperImg: [{
									image: 'https://wggdown.wanggougou.cn/webimg/wap20201212/guide/headPicture11.jpg',
									title: '“童欢乐▪共成长”公益活动'
								},
							{
									image: 'https://wggdown.wanggougou.cn/webimg/wap20201212/guide/headPicture2.jpg',
									title: '“童欢乐▪共成长”公益活动'
									},			
							],
			}
		},
		components: { myHeader },
		onLaunch () {
			uni.getSystemInfo({
			    success: function (res) {
					this.height = res.windowHeight;
			        console.log(res.windowHeight);
			    }
			});
		},
		methods:{
			goDelia(index){
				if(index==1){
					uni.reLaunch({
						url:"babyLand"
					})
				}
			}
		},
	}
</script>

<style scoped>
	/* 以下为视频CSS */
	
	.video-wrap {
		position: relative;
	}
	.headPicture{
		width: 750rpx;
		height: 1160rpx;
	}
	.title1{
		margin: 50rpx auto;
	}
	.vice-title{
		width: 360rpx;
		margin: 20rpx auto;
		font-size: 32rpx;
		font-family: Source Han Sans CN;
		font-weight: 500;
		color: #707070;
		opacity: 1;
		

	}
	.title1Img{
		width: 532rpx;
		height: 100rpx;
		display: block;
		margin: 0 auto;
		margin-bottom: 64rpx;
	}
	.title2Img{
		width: 316rpx;
		height: 100rpx;
		display: block;
		margin: 0 auto;
	}
	.title1_text{
		width: 670rpx;
		margin: 0 auto;
		font-size: 28rpx;
		font-family: Source Han Sans CN;
		font-weight: 400;
		line-height: 42rpx;
		color: #333333;
		opacity: 1;
	}
	.title2_text{
		width: 670rpx;
		margin: 0 auto;
		font-size: 24rpx;
		font-family: Source Han Sans CN;
		font-weight: 400;
		line-height: 36rpx;
		color: #707070;
		opacity: 1;

	}
	.pagesImg-box{
		width: 670rpx;
		height: 504rpx;
		margin: 0 auto;
		
		margin-bottom:44rpx ;
	}
	.pagesImg{
		width: 668rpx;
		height: 500rpx;
		background: rgba(0, 0, 0, 0);
		border: 6rpx solid #707070;
		box-shadow: 0px 60rpx 120rpx rgba(0, 0, 0, 0.2);
		opacity: 1;
		border-radius: 40rpx;
	}
	.pages{
		width: 688rpx;
		margin: 0 auto;
		display: flex;
		justify-content: space-around;
		flex-wrap: wrap;
	}
	.pageImg{
		width: 288rpx;height: 288rpx;
		margin-bottom: 40rpx;
	}
	.exhibition_box{
		width: 670rpx;
		margin: 0 auto;
		padding-bottom: 96rpx;
	}
	.exhibitionImg{
		width: 670rpx;
		height: 386rpx;
	}
</style>
