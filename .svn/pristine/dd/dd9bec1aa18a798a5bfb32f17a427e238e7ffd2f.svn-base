<template>
	<view class="e-page">
		<view id="fullpage" class="site__header">
		  <!-- #ifdef MP-WEIXIN -->
		 <view :style="style" class="weixin_yangshi">
		 			  <!-- <img v-show = "menu == 0" style="position:fixed;left: 17px;top: 24px;z-index: 9999;width: 25px;height: 25px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/menu.png" @click="showPopup" alt=""> -->
		 			  <img v-show = "1" class="weixin_header_img" src="https://wggdown.wanggougou.cn/webimg/wap20201014/header.png" @click="showPopup" alt="">
		 </view>
		   <!-- #endif -->
		   <!-- #ifdef H5 -->
		   <!-- <view :style="style" id="guide_header">
		   					  <img v-show = "menu == 0" class="guide_header_img1" src="../../static/index/menu.svg" @click="showPopup" alt="">
		   					  <img v-show = "menu"  src="../../static/index/menu.svg" @click="showPopup" alt="">
		   					  <img class="wanggougou_header_img" src="https://wggdown.wanggougou.cn/webimg/wap20201014/header.png" alt="">	  
		   </view> -->
		   <!-- 可改为组件了 下方 -->
		   <myHeader style="margin-bottom: 50rpx;"></myHeader>
		   <!-- #endif -->
		  <image style="width: 100%;height: auto;margin-top: 30px;" mode="widthFix" src="https://wggdown.wanggougou.cn/webimg/wap20201014/bj2.jpg"></image>
		  <view>
			  <view style="float: left;margin-left: 48px;margin-top: 36px;">
				  <img style="width: 64px;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/80x80.png" alt="">
			  </view>
			  <view style="float: left;margin-top: 44px;margin-left: 16px;color: rgba(80, 80, 80, 1);">
				  <view style="font-size: 22px;">旺狗狗数学</view>
				  <view style="font-size: 12px;color: rgba(255, 141, 26, 1);">学龄前孩子感兴趣的数学启蒙App</view>
			  </view>
		  </view>
		  <view class="text_535X2">
				Q萌有趣太空动物英雄形象，将抽象的数学思维生动形象化。以AI交互技术打造沉浸式学习场景，寓教于乐，
				<br>以AI交互技术打造沉浸式学习场景，寓教于乐，让孩子主动地获取知识。激发孩子学习兴趣，提升学习能力，拓展思维边界，让孩子轻松主动学习知识，健康快乐成长。
		  </view>
		  <view>
			  <view style="float: left;margin-left: 48px;margin-top: 15px;">
				  <img style="width: 142px;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/download.png" alt="">
				  <view class="text_533X2" @click="openDown">
					  下载App
				  </view>
			  </view>
			  <view style="float: right;">
				  <img style="width: 94px;margin-right: 48px;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/erweima/%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD.jpg" alt="">
			  </view>
		  </view>
		  <view class="box_541X3">
			  <view class="text_542X2" style="padding-top: 20px;">抓住学龄前启蒙儿童的黄金期</view>
			  <!-- <view class="text_542X2">孩子成长不是梦</view> -->

		  </view>
		   <video @click="play" class="course_image" id="myVideo" :show-play-btn="true" :show-center-play-btn="false" :src="videoUri" :controls="false" v-if="videoUri">
		   	<cover-view class="multi-list rate" :class="{ active: rateShow }">
		   		<cover-view
		   			v-for="(item, index) in ['0.5', '0.8', '1.0', '1.25', '1.5          ']"
		   			:key="index"
		   			class="multi-item rate"
		   			:data-rate="item"
		   			@tap="switchRate"
		   			:class="{ active: item == currentRate }"
		   		>
		   			{{ item }}
		   		</cover-view>
		   	</cover-view>
			<img v-show="!isPlay" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/play.png" style="position: relative;top: 50px;display: inline-block;width: 80px;height: 80px;left: 50%;transform: translate(-50%);z-index: 99;" alt=""  @click="play">
		   </video>
		   <view class="video-text">旺狗狗APP通过孩子感兴趣的动画、游戏，打造奇妙的娱学课堂。把枯燥的学习简单化、轻松化，在游戏中渗透逻辑思维，引导孩子养成爱动脑的学习思维能力</view>
		   <view>
				<img style="width: 100%;margin-top: 40px;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_1.png" alt="">
				<view style="margin-top: -30px;background-color: #CDE4FF;">
					<img style="width: 90%;margin-left: 5%;" :src="picUrl" alt="">
					<view >
					   <u-grid style="width: 90%;margin-left: 5%;padding: 40px 0;" :col="5"  >
							<u-grid-item style="background-color:rgba(0,0,0,0)">
								<img style="width: 42px;" v-show="checkType == 1" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_9.png',1)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_1.png" alt="">
								<img style="width: 42px;" v-show="checkType != 1" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_9.png',1)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_6.png" alt="">
								<view class="grid-text">爱数课堂</view>
							</u-grid-item>
							<u-grid-item style="background-color:rgba(0,0,0,0)">
								<img style="width: 42px;" v-show="checkType == 2" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_7.png',2)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_2.png" alt="">
								<img style="width: 42px;" v-show="checkType != 2" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_7.png',2)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_7.png" alt="">
								<view class="grid-text">星球冒险</view>
							</u-grid-item >
							<u-grid-item style="background-color:rgba(0,0,0,0)">
								<img style="width: 42px;" v-show="checkType == 3" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_6.png',3)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_3.png" alt="">
								<img style="width: 42px;" v-show="checkType != 3" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_6.png',3)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_8.png" alt="">
								<view class="grid-text">穿越太空</view>
							</u-grid-item>
							<u-grid-item style="background-color:rgba(0,0,0,0)">
								<img style="width: 42px;" v-show="checkType == 4" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_5.png',4)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_4.png" alt="">
								<img style="width: 42px;" v-show="checkType != 4" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_5.png',4)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_9.png" alt="">
								<view class="grid-text">自由训练</view>
							</u-grid-item>
							<u-grid-item style="background-color:rgba(0,0,0,0)">
								<img style="width: 42px;" v-show="checkType == 5" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_8.png',5)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_5.png" alt="">
								<img style="width: 42px;" v-show="checkType != 5" @click="showPicUrl('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_8.png',5)" src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/company_icon_10.png" alt="">
								<view class="grid-text">学习报告</view>
							</u-grid-item>
						</u-grid>
					</view>
				</view>
		   </view>
		   <view>
				<img style="width: 100%;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_3.png" alt="">
				<view style="background-color: #FFF7DF;padding-bottom: 40px;margin-top: -10px">
					<img style="width:  80%;margin-top: -180px;margin-left: 10%;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/people1.png" alt="">
				</view>
		   </view>
		   <view>
				<img style="width: 100%;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_2.png" alt="">
				<view style="background-color: #E3FFFF;padding-bottom: 40px;margin-top: -10px">
					<img style="width:  60%;margin-top: -120px;margin-left: 20%;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/people2.png" alt="">
				</view>
		   </view>
		   <view>
				<img style="width: 100%;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_4_1.png" alt="">
				<view style="background-color: #71FFAA;padding-bottom: 40px;margin-top: -10px;">
					<img style="width:  60%;margin-top: -160px;margin-left: 20%;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/people3.png" alt="">
				</view>
		   </view>
		   <view>
		   				<!-- <view >
		   					<img class="com_bottom_pic" src="https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_4_2.png" alt="">
		   				</view> -->
		   				<view class="wrap com_bottom">
		   					<view>
								<view style="float: left;">
									<img style="width: 72px;margin-left: 48px;margin-top: 20px;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/erweima/%E4%BA%A7%E5%93%81%E4%B8%8B%E8%BD%BD.jpg" alt="">
								</view>
								<view style="float: left;margin-top: 30px;">
									<view class="text_721X2">下载App</view>
									<view class="text_721X2">进入快乐学习之旅吧！</view>
								</view>
		   					</view>
		   					<view style="clear: both;float: left;margin-left: 48px;margin-top: 15px;">
		   					  <img style="width: 142px;" src="https://wggdown.wanggougou.cn/webimg/wap20201014/download.png" alt="">
		   					  <view class="text_533X3" @click="openDown">
		   						  下载App
		   					  </view>
		   					</view>
		   				</view>	
		   </view>
		 </view>
		<!-- <view>
		        <customSwiper :swiper-list="swiperList" />
		</view> -->
		<!-- #ifdef MP-WEIXIN -->
		<u-popup v-model="show" mode="top" width="100%" height="230px">
			<!-- <view style="height: 50px;"></view> -->
		<!-- #endif -->
		<!-- #ifdef H5 -->
		<u-popup v-model="show" mode="top" width="100%" height="100%">
		<!-- #endif -->
			<view class="guide_bg">
			  <img class="guide_body_img1" src="https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/icon.png" alt="">
			  <img class="guide_body_img2"  src="https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/menu_green.png" @click="showPopup" alt="">
			</view>
			<view><img class="icon_106X2" src="../../static/index/close.svg" alt="" @click="showPopup"></view>
			<view :class="!isshow_product?'checked':''" class="list-cell memu-text " @click="openUrl(1)">
				<text>
					首页
				</text>
			</view>
			<view :class="isshow_product?'checked':''" class="list-cell memu-text list_cell1"  @click="showProduct">
				线上产品
				<img v-if="isshow_product" class="icon_103X2" src="../../static/index/arrow_down_white.svg" alt="">
				<img v-if="!isshow_product" class="icon_103X2" src="../../static/index/arrow_down.svg" alt="">
			</view>
				<view v-show="isshow_product" class="wanggougou_login_img" @click="openUrl(2)">
					<img class="image_137X2"  src="https://wggdown.wanggougou.cn/webimg/wap20201014/icon/80x80.png" alt="">
					<view style="width: 100px;">旺狗狗</view>
				</view>
			<!-- <view class="list-cell memu-text" style="margin-top: 30px;" @click="openUrl(3)">
				关于我们
			</view> -->
			<view class="list-cell memu-text list_cell2"  @click="openUrl(4)">
				招商加盟
			</view>
			<view class="footer_chieseLanguage" @click="openUrl(4)">
				中文版
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
			videoUri: 'https://wggdown.wanggougou.cn/webvideo/ea1731e79115b7bd8782200d9c8090c31.mp4', // 视频地址
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
			current: 0,
			videoContext:null,
			isPlay:false,
			isshow_product:true,
			picUrl:"https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_9.png",
			checkType:1
		};
	},
	created () {
		this.onPageScroll
	},
	onReady: function (res) {
			this.videoContext = uni.createVideoContext('myVideo')
	},
	onShow() {
		// this.opacity = 0
		// this.menu = 0
		// this.style = {background: `rgba(255,255,255,0)`};
	},
	mounted() {
		// 保存数据到本地,选中导航是第几个
		 const info = 2;
		    localStorage.setItem('key', JSON.stringify(info));
	},
	
	methods: {
		onPageScroll: function(Object) {
		 // console.log(Object.scrollTop);//实时获取到滚动的值 
		 // if(Object.scrollTop > 500){
			// this.opacity = Math.abs(Object.scrollTop -500) / 250;
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
		},
		openUrl(index){
			this.show =false
			if(index == 1){
				uni.redirectTo({
					url:"./index"
				})
			}else if(index == 2){
		
			}
			else if(index == 3){
				uni.redirectTo({
					url:"./investment"
				})
			}
			else if(index == 4){
				uni.redirectTo({
					url:"./investment"
				})
			}
			
		},
		openDown(){
			window.location.href = "https://www.wanggougou.cn/download.html";
		},
		play(){
			if(this.isPlay){
				this.videoContext.pause()
				this.isPlay = false
			}else{
				this.videoContext.play()
				this.isPlay = true
			}
			
		},
		showProduct(){
			if(this.isshow_product){
				this.isshow_product = false
			}else{
				this.isshow_product = true
			}
		},
		showPicUrl(picUrl,checkType){
			console.log(checkType)
			this.picUrl = picUrl
			this.checkType = checkType
		}
	}
};
</script>

<style>
/* 以下为视频CSS */
.course_image {
	width: 80%;
	height: 170px;
	margin-left: 10%;
	border-radius: 20rpx;
	margin-top: -28px;
}
.video-control {
	background-color: rgba(0, 0, 0, 0.1);
	height: 80rpx;
	position: absolute;
	top:0;
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
	.uni-video-cover-play-button{
		background-image: url("https://wggdown.wanggougou.cn/webimg/wap20200911/index/play.png") !important
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
	.text_533X3{
		width: 108px;
		height: 23px;
		padding-top:2px;
		margin-top: 16px;
		color: rgba(255, 255, 255, 1);
		background-color: rgba(255, 195, 0, 1);
		border-radius: 16px;
		font-size: 12px;
		line-height: 150%;
		text-align: center;
	}
	.box_541X2{
		display:inline-block;
		width: 100%;
		height: 113px;
		margin-top: 44px;
		color: rgba(80, 80, 80, 1);
		/* background-color: rgba(67, 207, 124, 1); */
		font-size: 14px;
		line-height: 150%;
		text-align: center;
	}
	.box_541X3{
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
	.grid-text{
		margin-top: 15px;
		font-size: 10px;
	}
	.com_bottom{
		position: relative;
		top: 0;
		z-index: 999;
		background: url('https://wggdown.wanggougou.cn/webimg/wap20201014/company_bj_4_2.png');
		background-size: 100% auto;
		min-height: 300px;
	}
	.com_bottom_pic{
		width: 100%;
		float: left;
		 display: inline-block;
		 
	}
	.text_721X2{
		font-size: 12px;
		line-height: 150%;
		padding-left: 28px;
		text-align: left;
	}
	.weixin_yangshi{height: 68px;position:fixed;top: 0px;left: 0px;z-index:99999;width: 100%;background-color: #FFFFFF;}
	.weixin_header_img{position:fixed;left: 17px;top: 28px;z-index: 9999;width: 25px;height: 25px;}
	
	#guide_header{
		 height: 54px;
		 position:fixed;
		 top: 0px;
		 left: 0px;
		 z-index: 99999;
		 width: 100%;
		 background-color: #FFFFFF;
	}
	#guide_header>.guide_header_img1{
		position:fixed;left: 20px;top: 14px;z-index: 9999;
		width: 25px !important;
		height: 25px !important;
	}
	#guide_header>.guide_header_img2{
		position:fixed;left: 20px;top: 14px;z-index: 9999;width: 25px;height: 25px;
	}
	 .wanggougou_header_img{
		position:fixed;left: 36%;top: 15px;z-index: 9999;width: 126px;height: 23px;
	}
	
@import "../../static/css/index";
</style>
