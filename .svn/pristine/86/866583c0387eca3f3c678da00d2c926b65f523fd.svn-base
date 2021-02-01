<template>
	<view class="e-page">
		<view id="fullpage" class="site__header">
		   <!-- #ifdef MP-WEIXIN -->
		   <view :style="style" style="height: 68px;position:fixed;top: 0px;left: 0px;z-index:99999;width: 100%;background-color: #FFFFFF;" >
		   			  <!-- <img v-show = "menu == 0" style="position:fixed;left: 17px;top: 24px;z-index: 9999;width: 25px;height: 25px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/menu.png" @click="showPopup" alt=""> -->
		   			  <img v-show = "1" style="position:fixed;left: 17px;top: 28px;z-index: 9999;width: 25px;height: 25px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/menu_green.png" @click="showPopup" alt="">
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
		   <image style="width: 100%;height: auto;" mode="widthFix" src=
"https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg1.jpg"></image>
		   <image style="width: 100%;height: auto;" mode="widthFix" src=
"https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg2.jpg"></image>
		    <image style="width: 100%;height: auto;" mode="widthFix" src=
"https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg3.png"></image>
			<!-- <view class="">
				<img style="width: 100%;height: auto;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg4.png" alt="">
				<img style="width: 100%;height: auto;margin-bottom: -12rpx;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg41.png" alt="">
			</view> -->
			<image style="width: 100%;height: auto;margin-bottom: -8rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg4.png"></image>
			<image style="width: 100%;height: auto;margin-bottom: -12rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg41.png" @click="openZL('https://www.zhipin.com/job_detail/7e24f4a012f451973nBz3Nq0E1c~.html?ka=search_list_jname_2_blank&lid=nlp-QmMzaY7DhA.search.2')"></image>
			<image style="width: 100%;height: auto;margin-bottom: -12rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg42.png" @click="openZL('https://www.zhipin.com/job_detail/a08ff99387fad51333xy3dq1F1I~.html?ka=search_list_jname_10_blank&lid=nlp-QmMzaY7DhA.search.10')"></image>
			<image style="width: 100%;height: auto;margin-bottom: -12rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg43.png" @click="openZL('https://www.zhipin.com/job_detail/11e1a84392b5244a3ndz3NW0ElU~.html?ka=search_list_jname_9_blank&lid=nlp-QmMzaY7DhA.search.9')"></image>
			<image style="width: 100%;height: auto;margin-bottom: -12rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg44.png" @click="openZL('https://www.zhipin.com/job_detail/11e1a84392b5244a3ndz3NW0ElU~.html?ka=search_list_jname_9_blank&lid=nlp-QmMzaY7DhA.search.9')"></image>
			<image style="width: 100%;height: auto;margin-bottom: -12rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg45.png" @click="openZL('https://www.zhipin.com/job_detail/cbcb8f93c6a3da303nBy2d64EFA~.html?ka=search_list_jname_14_blank&lid=nlp-QmMzaY7DhA.search.14')"></image>
			<image style="width: 100%;height: auto;margin-bottom: -12rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/join/bg46.png" @click="openZL('https://www.zhipin.com/job_detail/ba3a059d058369853nBy2dm9E1o~.html?ka=search_list_jname_15_blank&lid=nlp-QmMzaY7DhA.search.15')"></image>
			<image style="width: 100%;height: auto;margin-bottom: -12rpx;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/bg7.png"></image>
		 </view>
		<!-- <view>
		        <customSwiper :swiper-list="swiperList" />
		</view> -->
		<!-- #ifdef MP-WEIXIN -->
		<u-popup v-model="show" mode="top" width="100%" height="230px">
			<view style="height: 50px;"></view>
		<!-- #endif -->
		<!-- #ifdef H5 -->
		<u-popup v-model="show" mode="top" width="100%" height="270px">
		<!-- #endif -->
			<view style="height: 54px;width: 100%;background-color: #FFFFFF;">
			  <img style="position:relative;left: 17px;top: 7px;z-index: 9999;width: 66px;height: 40px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/icon.png" alt="">
			  <img style="position:fixed;right: 20px;top: 14px;z-index: 9999;width: 25px;height: 25px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/menu_green.png" @click="showPopup" alt="">
			</view>
			<view class="list-cell memu-text" @click="openUrl(1)">
				<text>
					首页
				</text>
				
			</view>
			<view class="list-cell memu-text" @click="openUrl(2)">
				企业介绍
				
			</view>
			<view class="list-cell memu-text" @click="openUrl(3)">
				招商加盟
			</view>
			<view class="list-cell memu-text" style="background: #F4FBEB;" @click="openUrl(4)">
				加入我们
				<view style="height: 2px;background-color: #97D937;width: 34px;border-radius: 1px;margin: 0 auto;margin-top: 3px;"></view>
			</view>
			
		</u-popup>
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
			swiperList: [{
				type: 'image',
				url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big84000.jpg'
			}, {
				type: 'image',
				url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big37006.jpg',
			}, {
				type: 'image',
				url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big39000.jpg'
			}, {
				type: 'image',
				url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big10001.jpg'
			}, {
				type: 'image',
				url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big25011.jpg'
			}, {
				type: 'image',
				url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big21016.jpg'
			}, {
				type: 'image',
				url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big99008.jpg'
			}],
			list: [{
				name: 'level1.png'
			}, {
				name: 'level2.png'
			}, {
				name: 'level3.png'
			}, {
				name: 'level4.png'
			}],
			current: 0
		};
	},
	created () {
		this.onPageScroll
	},
	methods: {
		onPageScroll: function(Object) {
		 //console.log(Object.scrollTop);//实时获取到滚动的值 
		 if(Object.scrollTop > 200){
			this.opacity = Math.abs(Object.scrollTop -200) / 250;
			this.style = {background: `rgba(255,255,255,${this.opacity})`}; 
			this.menu = 1;
		 }else{
			 this.opacity = 0
			 this.style = {background: `rgba(255,255,255,0)`}; 
			 this.menu = 0;
		 }
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
		// 		uni.redirectTo({
		// 			url:"./investment"
		// 		})
		// 	}
		// 	else if(index == 4){
		// 	}
			
		// },
		openZL(obj){
			window.location.href = obj;
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
		border-bottom:1px solid #eee;
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
@import "../../static/css/index";
</style>
