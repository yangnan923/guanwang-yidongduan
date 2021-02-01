<template>
	<view class="e-page">
		<view id="fullpage" class="site__header">
		   <!-- #ifdef MP-WEIXIN -->
		   <view :style="style" class="investment_ini1" >
		   			  <!-- <img v-show = "menu == 0" style="position:fixed;left: 17px;top: 24px;z-index: 9999;width: 25px;height: 25px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/menu.png" @click="showPopup" alt=""> -->
		   			  <img v-show = "1" style="position:fixed;left: 17px;top: 28px;z-index: 9999;width: 25px;height: 25px;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/header.png" @click="showPopup" alt="">
		   </view>
		    <!-- #endif -->
		    <!-- #ifdef H5 -->
		   <!-- <view :style="style" id="guide_header">
		    					  <img v-show = "menu == 0" class="guide_header_img1" src="../../static/index/menu.svg" @click="showPopup" alt="">
		    					  <img v-show = "menu"  src="../../static/index/menu.svg" @click="showPopup" alt="">
		    					  <img class="wanggougou_header_img" src="https://wggdown.wanggougou.cn/webimg/wap20201014/header.png" alt="">	  
		    </view> -->
		    <!-- 可改为组件了 下方 -->
		     <myHeader style="margin-bottom: 100rpx;"></myHeader>
		   <!-- #endif -->
		   <image style="width: 100%;height: auto;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/investment/bg1.jpg"></image>
		   <image style="width: 100%;height: auto;margin-bottom: 29px;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/investment/b33x.png"></image>
		   <mosowe-swiper
		       :lists="banner1"
		       :touchable="false"
		       indicator=""
		       imageKey="image"
		       previewImage
		       pyramid
		   	:autoplay="false"
		   	:height="600"
		   	:mheight="600"
		     pyramidMargin="150rpx"
		       />
			<image style="width: 100%;height: auto;margin: 29px 0;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/investment/bg3.png"></image>
		    <image style="width: 100%;height: auto;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/investment/bg4.jpg"></image>
			<view class="wgg-text">用户规模增长迅速，市场规模上升，2020年在线教育市场规模将达4538亿元。</view>
			<image style="width: 100%;height: auto;margin: 29px 0;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/investment/b13x.png"></image>
		    <mosowe-swiper
		        :lists="banner2"
		        :touchable="false"
		        indicator=""
		        imageKey="image"
		        previewImage
		        pyramid
		    	:autoplay="false"
		    	:height="540"
				:mheight="540"
		        pyramidMargin="150rpx"
		        
		        />
				
				<!-- @change="bannerChange" 这句代码是上个标签的错误代码-->
			<image style="width: 100%;height: auto;margin: 29px 0;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/investment/b23x.png"></image>
			<mosowe-swiper
			    :lists="banner3"
			    :touchable="false"
			    indicator=""
			    imageKey="image"
			    previewImage
			    pyramid
				:autoplay="false"
				:height="540"
				:mheight="540"
			    pyramidMargin="150rpx"
			     />
			<view class="footer_bg_all">
						   <view style="text-align: center;">
									   <text class="text_585X2">@2019-2020 重庆旺狗狗科技有限公司 所有权保留</text>  
						   </view>
						   <view style="text-align: center;">
									   <text class="text_585X2">渝ICP备19012451号-1</text>
						   </view>
			</view>
		 </view>
		<!-- <view>
		        <customSwiper :swiper-list="swiperList" />
		</view> -->
		<!-- #ifdef MP-WEIXIN -->
		<u-popup v-model="show" mode="top" width="100%" height="230px">
			<view style="height: 50px;"></view>
		<!-- #endif -->
		<!-- #ifdef H5 -->
		<u-popup v-model="show" mode="top" width="100%" height="100%">
		<!-- #endif -->
			<view style="height: 54px;width: 100%;background-color: #FFFFFF;">
			  <img style="position:relative;left: 17px;top: 7px;z-index: 9999;width: 66px;height: 40px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/icon.png" alt="">
			  <img style="position:fixed;right: 20px;top: 14px;z-index: 9999;width: 25px;height: 25px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/menu_green.png" @click="showPopup" alt="">
			</view>
			<view><img class="icon_106X2" src="../../static/index/close.svg" alt="" @click="showPopup"></view>
			<view class="list-cell memu-text" @click="openUrl(1)">
				<text>
					首页
				</text>
			</view>
			<view :class="isshow_product?'checked':''" class="list-cell memu-text" style="margin-top: 30px;padding-top: 5px;" @click="showProduct">
				线上产品
				<img v-if="isshow_product" class="icon_103X2" src="../../static/index/arrow_down_white.svg" alt="">
				<img v-if="!isshow_product" class="icon_103X2" src="../../static/index/arrow_down.svg" alt="">
			</view>
				<view v-show="isshow_product" style="background-color: #E7E6E6;padding: 40px 120px;margin-left:calc(50% - 144px);margin-right:calc(50% - 144px);margin-top: 30px;" @click="openUrl(2)">
					<img class="image_137X2"  src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/80x80.png" alt="">
					<view style="width: 100px;">旺狗狗</view>
				</view>
			<!-- <view class="list-cell memu-text" style="margin-top: 30px;" @click="openUrl(3)">
				关于我们
			</view> -->
			<view :class="!isshow_product?'checked':''" class="list-cell memu-text" style="margin-top: 30px;" @click="openUrl(4)">
				招商加盟
			</view>
			<view style="position: fixed;bottom: 20px;left:calc(50% - 19px);color: rgba(80, 80, 80, 1)" @click="openUrl(4)">
				中文版
			</view>
		</u-popup>
		<view @click="openKefu">
			<img style="position:fixed;bottom: 30px;right: 10px;z-index: 9999;width: 90px;height: 100px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/investment/kefu2x.png" alt="">
		</view>
	</view>

</template>

<script>
	import customSwiper from '@/components/blackmonth-swiper/index';
import myHeader from '@/components/my_header/my_header';
export default {
	components: { customSwiper,myHeader },
	data() {
		return {
			videoUri: 'https://wggdown.oss-cn-zhangjiakou.aliyuncs.com/video/aaaa.mp4', // 视频地址
			rateShow: false, // 倍速浮层
			currentRate: 1.0, // 默认倍速
			show: false,
			style: {},
			opacity: 0,
			menu:0, //分类按钮状态
			banner1: [
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/zhengce1.png',
					url : 'http://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/jyzt_2018n/2018_zt07/zt1807_dbwy/201803/t20180312_329681.html'
			    },
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/zhengce2.png',
					url : 'http://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/s5987/201909/t20190930_401761.html'
			    },
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/zhengce3.png',
					url : 'http://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/201703/t20170315_299716.html'
			    },
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/zhengce4.png',
					url : 'http://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/jyzt_2018n/2018_zt07/zt1807_dbwy/201803/t20180312_329681.html'
			    }
			],
			banner2: [
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/youshi13x.png',
			    },
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/youshi24x.png',
			    },
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/youshi33x.png',
			    }
			],
			banner3: [
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/biaoti13x.png',
			    },
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/biaoti43x.png',
			    },
			    {
			        image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/biaoti33x.png',
			    },
				{
				    image: 'https://wggdown.wanggougou.cn/webimg/wap20200911/investment/biaoti23x.png',
				}
			],
			current: 0,
			isshow_product:false
		};
	},
	created () {
		this.onPageScroll
	},
	methods: {
		onPageScroll: function(Object) {
		 //console.log(Object.scrollTop);//实时获取到滚动的值 
		 // if(Object.scrollTop > 200){
			// this.opacity = Math.abs(Object.scrollTop -200) / 250;
			// this.style = {background: `rgba(255,255,255,${this.opacity})`}; 
			// this.menu = 1;
		 // }else{
			//  this.opacity = 0
			//  this.style = {background: `rgba(255,255,255,0)`}; 
			//  this.menu = 0;
		 // }
		},
		_initBody () {
			this.mainBodyScroll = new BScroll(this.$refs.mainBody, {
				click: true,
				probeType: 3
			});
			this.mainBodyScroll.on('scroll', (pros) => {
				
			});
		},
		// 显示倍速浮层
		showSwitchRate(rate) {
			let that = this;
			console.log('rateShow');
			that.rateShow = true;
		},
		// 切换倍速
		switchRate(e) {
			let that = this;
			let rate = Number(e.currentTarget.dataset.rate);
			that.currentRate = rate;
			that.rateShow = false;
			this.videoContext.playbackRate(rate);
		},
		showPopup(){
			if(this.show){
				this.show =false
			}else{
				this.show =true
			}
		},
		change(index) {
			this.current = index;
			console.log(this.current)
		},
		// openUrl(index){
		// 	this.show =false
		// 	if(index == 1){
		// 		uni.redirectTo({
		// 			url:"./index"
		// 		})
		// 	}else if(index == 2){
		// 		uni.redirectTo({
		// 			url:"./company"
		// 		})
		// 	}
		// 	else if(index == 3){

		// 	}
		// 	else if(index == 4){
				
		// 	}
			
		// },
		openKefu(){
			window.location.href = "https://cschat-ccs.aliyun.com/index.htm?tntInstId=_21mrw8e&scene=SCE00008178";
		},
		showProduct(){
			if(this.isshow_product){
				this.isshow_product = false
			}else{
				this.isshow_product = true
			}
		}
	}
};
</script>

<style>
/* 以下为视频CSS */
.course_image {
	width: 90%;
	height: 200px;
	margin-left: 5%;
	border-radius: 20rpx;
}
.video-control {
	background-color: rgba(0, 0, 0, 0.1);
	height: 80rpx;
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	z-index: 997;
}
.video-wrap {
	position: relative;
}
.multi-list.full-screen.vertical {
	height: 100vh !important;
	padding: 8vh 0;
}
.multi-list.full-screen.horizontal {
	height: 100vw !important;
	padding: 8vw 0;
}
.multi {
	position: absolute;
	right: 30rpx;
	top: 50%;
	transform: translateY(-50%);
	z-index: 998;
	width: 100rpx;
	color: #fff;
	padding: 10rpx 0;
	text-align: center;
	transition: color ease 0.3s;
}
.multi.rate {
	right: 30rpx;
}
.multi-list {
	position: absolute;
	height: 100%;
	width: 0;
	background-color: rgba(0, 0, 0, 0.65);
	top: 0;
	right: 0;
	transition: width 0.3s ease;
	z-index: 999;
	box-sizing: border-box;
	padding: 50rpx 0;
}
.multi-list.rate {
	padding: 25rpx 0;
}
.multi-list.active {
	width: 300rpx;
}
.multi-item {
	text-align: center;
	color: #fff;
	line-height: 80rpx;
	transition: color ease 0.3s;
}
.multi-item.rate {
	line-height: 70rpx;
}
.multi-item:hover,
.multi:hover {
	color: #00d8ff;
}
.multi-item.active {
	color: #00d8ff;
} /* 视频CSS结束 */
.list-cell {
		/* display: flex;
		box-sizing: border-box; */
		padding: 10px 24rpx;
		overflow: hidden;
		color: #323233;
		font-size: 14px;
		line-height: 24px;
		background-color: #fff;
		/* border-bottom:1px solid #eee; */
		text-align: center;
	}
	.memu-text{
		font-weight: bold;color: #7B7B7B;font-size: 15px;
		height: 54px;
	}
	.video-text{
		margin: 28px 20px;
		text-align: center;
		font-size: 13px;
		font-weight: 400;
		color: #7B7B7B;
		
line-height:19px;
	}
	.wgg-text{
		width: 90%;
		font-size: 13px;
		margin: 29px 0;
		margin-left: 5%;
		font-family: Microsoft YaHei;
		font-weight: 400;
		line-height: 19px;
		color: #757575;
		
	}
	.hezuo{
		width: 80%;
		margin: 10px 32px;
		left: 32px;
		top: 376px;
		color: rgba(80, 80, 80, 1);
		font-size: 12px;
		height: 200%;
			
	}
	.text_417X2{
		width: 80%;
		margin: 35px 32px;
		left: 32px;
		top: 420px;
		color: rgba(80, 80, 80, 1);
		font-size: 12px;
		line-height: 180%;
	}
	.image_115X2{
		width: 58px;
		height: 51px;
		left: calc(50% - 29px);
		top: 0px;
		position: relative;
	
	}
	.image_106X2{
		width: 58px;
		height: 36px;
		left: calc(50% - 29px);
		top: 15px;
		position: relative;
	}
	.text_460X2{
		position: relative;
		top: 20px;
		left: 8px;
	}
	.text_461X2{
		position: relative;
		top: 35px;
		left: 8px;
	}
	.text_585X2{
		height: 56px;
		top: 584px;
		color: rgba(80, 80, 80, 1);
		font-size: 7px;
		line-height: 200%;
		text-align: center;
	}
	.icon_106X2{
		width: 24px;
		height: 24px;
		left: calc(100% - 50px);
		top: 0px;
		font-size: 24px;
		color: rgba(153, 153, 153, 1);
		position: relative;
	}
	.checked{
		width: 158px;
		height: 32px;
		margin: 0 auto;
		color: rgba(33, 32, 32, 1);
		background-color: rgba(255, 195, 0, 1);
		border-radius: 16px;
		font-size: 14px;
		line-height: 100%;
		color: #FFFFFF;
	}
	.icon_103X2{
		width: 15px;
		height: 15px;
		left: 213px;
		top: 0px;
		-webkit-transform: rotate(90deg);
		transform: rotate(90deg);
		font-size: 15px;
		color: rgba(83, 78, 78, 1);
	}
	.image_137X2{
		width: 47px;
		height: 47px;
		
		
	}
	.text_535X2{
		margin:10px 48px;
		display:inline-block;
		color: rgba(80, 80, 80, 1);
		font-size: 12px;
		line-height: 150%;
	}
	.text_533X2{
		width: 155px;
		height: 33px;
		padding-top: 5px;
		margin-top: 16px;
		color: rgba(255, 255, 255, 1);
		background-color: rgba(255, 195, 0, 1);
		border-radius: 16px;
		font-size: 14px;
		line-height: 150%;
		text-align: center;
	}
	.box_541X2{
		display:inline-block;
		width: 100%;
		height: 113px;
		margin-top: 44px;
		color: rgba(80, 80, 80, 1);
		background-color: rgba(67, 207, 124, 1);
		font-size: 14px;
		line-height: 150%;
		text-align: center;
	}
	.text_542X2{
		width: 100%;
		color: rgba(255, 255, 255, 1);
		font-size: 17px;
		line-height: 150%;
		text-align: center;
	}
	.text_542X2_small{
		width: 100%;
		color: rgba(255, 255, 255, 1);
		font-size: 13px;
	}
	.text_589X2{
		width: 100%;
		color: rgba(59, 57, 57, 1);
		font-size: 13px;
		line-height: 150%;
		text-align: center;
	}
	.text_565X2{
		width: 100%;
		color: rgba(80, 80, 80, 1);
		font-size: 12px;
		line-height: 150%;
		text-align: center;
	}
	.investment_ini1{height: 68px;position:fixed;top: 0px;left: 0px;z-index:99999;width: 100%;background-color: #FFFFFF;}
	
	.footer_bg_all{background-color: #FFFFFF;margin-top: 60px;display: inline-block;width: 100%;}
@import "../../static/css/index";
</style>
