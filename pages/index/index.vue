<template>
	<view class="e-page"  style="background-color: #F5F8FA;">
		<view id="fullpage" class="site__header">
		   <!-- #ifdef MP-WEIXIN -->
		 <!-- <view :style="style" class="weixin_yangshi">
			  <img v-show = "1" class="weixin_header_img" src="https://wggdown.wanggougou.cn/webimg/wap20201014/header.png" @click="showPopup" alt="">
		  </view> -->
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
		   <image src="https://wggdown.wanggougou.cn/webimg/wap20201212/indexPages111111.jpg" class="indexPages"></image>
		   <view class="indexPages2">
				<view class="wrap_box1">
					<u-swiper :list="swiperImg1" height="308" title="true" mode="none"></u-swiper>
					<view class="">
					</view>
				</view>
				
				<view class="wrap_box2">
						<u-swiper :list="swiperImg" :effect3d="true" :height="246" :effect3d-previous-margin=200 mode="none"></u-swiper>
					</view>
					<!-- 轮播指示点样式修改 -->
					<view class="dots">
						<block v-for="(item,index) in swiperImg.length" :key="index">
							<view class="dot" :class="index==swiperCurrent ? ' active' : ''"></view>
						</block>
					</view>
		   </view>
		   
		   <view>
			   
			   
			 
		   </view>
		   
		 </view>
		<!-- <view>
		        <customSwiper :swiper-list="swiperList" />
		</view> -->
		<!-- #ifdef MP-WEIXIN -->
		<!-- <u-popup v-model="show" mode="top" width="100%" height="230px">
			<!-- <view style="height: 50px;"></view> -->
		<!-- #endif -->
		<!-- #ifdef H5 -->
		<!-- <u-popup v-model="show" mode="top" width="100%" height="100%"> -->
		<!-- #endif
			<view class="guide_bg">
			  <img class="guide_body_img1" src="https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/icon.png" alt="">
			  <img class="guide_body_img2"  src="<strong>https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/menu_green.png</strong>" @click="showPopup" alt="">
			</view>
			<view><img class="icon_106X2" src="../../static/index/close.svg" alt="" @click="showPopup"></view>
			<view :class="!isshow_product?'checked':''" class="list-cell memu-text" @click="openUrl(1)">
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
			
			<view class="list-cell memu-text list_cell2"  @click="openUrl(4)">
				招商加盟
			</view>
			<view class="footer_chieseLanguage" @click="openUrl(4)">
				中文版
			</view>
		</u-popup> -->
		<!-- <view @click="openDown">
			<img style="position:fixed;bottom: 0px;z-index: 9999;width: 100%;height: 65px;" src="https://wggdown.wanggougou.cn/webimg/wap20200911/index/down.png" alt="">
		</view> -->
	</view>
	
</template>

<script>
	import customSwiper from '@/components/blackmonth-swiper/index';
	import myHeader from '@/components/my_header/my_header';
export default {
	components: { customSwiper,myHeader },
	data() {
		return {
			videoUri: 'https://down.wanggougou.cn/webimg/video/main.mp4', // 视频地址
			rateShow: false, // 倍速浮层
			currentRate: 1.0, // 默认倍速
			show: false,
			style: {},
			opacity: 0,
			menu:0, //分类按钮状态
			swiperCurrent:0,
			isactive:1,//向子组件传值
			
			swiperImg1: [{
									image: 'https://wggdown.wanggougou.cn/webimg/wap20201212/wrap1Img1.png',
									title: '“童欢乐▪共成长”公益活动'
								},
								{
									image: 'https://wggdown.wanggougou.cn/webimg/wap20201212/wrap1Img2.png',
									title: '灯光篮球场公益活动'
								},
								{
									image: 'https://wggdown.wanggougou.cn/webimg/wap20201212/wrap1Img3.png',
									title: '献爱心进校园儿童教育活动'
								},
								{
									image: 'https://wggdown.wanggougou.cn/webimg/wap20201212/wrap1Img4.png',
									title: '用爱心点燃留守儿童的希望'
								},
								{
									image: 'https://wggdown.wanggougou.cn/webimg/wap20201212/wrap1Img5.png',
									title: '中国青少年健康关爱课堂公益行'
								}
							],
			swiperImg: [
				'https://wggdown.wanggougou.cn/webimg/wap20201014/erweima/biao8%25403x.png',					
				'https://wggdown.wanggougou.cn/webimg/wap20201014/erweima/biao9%25403x.png',
				'https://wggdown.wanggougou.cn/webimg/wap20201014/erweima/biao10%25403x.jpg',	
			],
			list: [{
				name: 'level1.png'
			}, {
				name: 'level2.png'
			}, {
				name: 'level3.png'
			}, {
				name: 'level4.png'
			}],
			banner2: [
						    {
						        image: 
			'https://wggdown.wanggougou.cn/webimg/wap20200911/company/b13x.png',
								text:"优质平台产品",
								des:""
						    },
						    {
						        image: 
			'https://wggdown.wanggougou.cn/webimg/wap20200911/company/b23x.png',
								text:"重庆创意50强",
								des:""
						    },
							{
							    image: 
			'https://wggdown.wanggougou.cn/webimg/wap20200911/company/b33x.png',
								text:"重庆互联网百强",
								des:""
							},
							{
							    image: 
			'https://wggdown.wanggougou.cn/webimg/wap20200911/company/b43x.png',
								text:"社会满意度证书",
								des:""
							},
							{
							    image: 
			'https://wggdown.wanggougou.cn/webimg/wap20200911/company/b53x.png',
								text:"教育成长30强",
								des:""
							},
							{
							    image: 
			'https://wggdown.wanggougou.cn/webimg/wap20200911/company/b63x.png',
								text:"信赖知名教育品牌",
								des:""
							},
							{
							    image: 
			'https://wggdown.wanggougou.cn/webimg/wap20200911/company/b73x.png',
								text:"知名教育平台",
								des:""
							},
						],
			current: 0,
			videoContext:null,
			isPlay:false,
			isshow_product:false,
			dotStyle: false,
		};
	},
	created () {
		this.onPageScroll;
	},
	onReady: function (res) {
			this.videoContext = uni.createVideoContext('myVideo')
	},
	onShow() {
		// this.opacity = 0
		// this.menu = 0
		// this.style = {background: `rgba(255,255,255,0)`};
		
	
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
		DotStyle(e) {
			this.dotStyle = e.detail.value
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
			this.isshow_product = false
			if(this.show){
				this.show =false
			}else{
				this.show =true
			}
		},
		change(index) {
			this.current = index;
		},
		// openUrl(index){
		// 	this.show =false
		// 	if(index == 1){
		// 		this.isshow_product = false
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
		// 		uni.redirectTo({
		// 			url:"./investment"
		// 		})
		// 	}
			
		// },
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
		changeSwiper(e) {
			this.swiperCurrent = e.detail.current;
		}
	}
};
</script>

<style scoped>
/* 以下为视频CSS */
.indexPages{
	width: 750rpx;
	height: 6350rpx;
}
.indexPages2{
	width: 750rpx;
	height: 2336rpx;
	background-image: url("https://wggdown.wanggougou.cn/webimg/wap20201212/about1.png");
	background-size: 100%;
	background-repeat: no-repeat;
	position: relative;
}
.wrap_box1{
	width: 670rpx;
	height: 308rpx;
	background: #FFFFFF;
	box-shadow: 0px 40px 60px #DFE7FC;
	opacity: 1;
	border-radius: 10px;
	position: absolute;
	left: 50%;
	transform: translateX(-50%);  
	top: 200rpx;
}.wrap_box2{
	width: 670rpx;
	height: 246rpx;
	background: #FFFFFF;
	box-shadow: 0px 40px 60px #DFE7FC;
	opacity: 1;
	border-radius: 10px;
	position: absolute;
	left: 50%;
	transform: translateX(-50%);  
	top: 836rpx;
}
.course_image {
	width: 90%;
	height: 212px;
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
	color: #00d8ff !important;
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
		/* height: 84px; */
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
		text-align: center;
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
		height: 51px;
		left: calc(50% - 29px);
		top: 0px;
		position: relative;
	}
	.text_460X2{
		font-size: 12px;
		position: relative;
		top: 20px;
		left: 0;
	}
	.text_461X2{
		font-size: 12px;
		/* position: relative; */
		text-align: center;
		top: 20px;
		left: 0;
	}
	.text_585X2{
		display: inline-block;
		width: 100%;
		top: 584px;
		color: rgba(80, 80, 80, 1);
		font-size: 7px;
		line-height: 100%;
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

	.weixin_yangshi{height: 100rpx;position:fixed;top: 0px;left: 0px;z-index:99999;width: 100%;background-color: #FFFFFF;}
	.weixin_header_img{position:fixed;left: 56rpx;top: 36rpx;z-index: 9999;width: 25px;height: 25px;}
	/* 以下是10.29号标签内css 改下的 */
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
	.web_img1{
		display: block;
		width: 100%;height: auto;margin-top: 50px;
		position: relative;
	}
	.web_img2{
		display: block;
		width: 100%;height: auto;margin-top: 30px;		
		position: relative;
	}
	.aboutWe-div1{
		height: 5px;width: 100%;background-color: #C0C0C0;float: left;
	}
	/* .aboutWe-div2{
		height: 5px;width: 35%;background-color: #31d8a9;float: left;
	} */
	.aboutWe-text{
		text-align: center;font-size: 14px;margin-bottom: 10px;
	}
	.footer_bg_all{
		background-color: #f3f3f3;margin: 0;
	}
	.footer_bg1{
		height: 3px;width: 100%;background-color: #f3f3f3;float: left;
	}
	/* .footer_bg2{
		height: 3px;width: 35%;background-color: #31d8a9;float: left;
	} */
	.title_text_box{
		padding-top: 60px;padding-bottom: 30px;text-align: center;
	}
	.title_text{
	letter-spacing: 2px;color: rgba(0, 0, 0, 1);font-size: 17px;font-weight: bold;
	}
	.want_personnel_box{
		background-color: #F3F3F3 !important;
		width: 128px !important;
	}
.image_307X2{
	width: 58px;
	height: 51px;
	left: 87px;
	top: 13px;
	margin-bottom: 6px;
}
.image_302X2{
	width: 60px;
	height: 38px;
	margin-bottom: 16px;
}
.image_304X2{
	width: 45px;
	height: 44px;
	left: 94px;
	top: 142px;
	margin-bottom: 22px;
}
.image_306X2{
	width: 76px;
	height: 51px;
	left: 211px;
	top: 136px;
	margin-bottom: 18px;
}
.image_303X2{
	width: 58px;
	height: 38px;
	left: 88px;
	top: 291px;
	margin-bottom: 13px;
}
.image_305X2{
	width: 53px;
	height: 32px;
	left: 219px;
	top: 298px;
	margin-bottom: 16px;
}
	.grid-text{
		width: 65px;
			height: 50px;
			left: 88px;
			top: 81px;
			color: rgba(80, 80, 80, 1);
			font-size: 13px;
			line-height: 130%;
			text-align:center;
	}
	.callWe_box{
		padding-top: 30px;
	}
	.callWe_text{
		margin-left: 32px;letter-spacing: 2px;color: rgba(0, 0, 0, 1);font-size: 12px;font-weight: bold;
	}
	.official_account_box{
		width: 30%;margin-bottom: 60px;
		float: left;
		margin-top: 60px;
		margin-left: 30px;
	}
	.official_account_img_box{
	margin-left: calc(50% - 35px);
	}
	.official_account_text{
		text-align: center;margin-top: 10px;
		font-size: 11px;
	}
	.ownership{
		 background-color: #f3f3f3;padding-top: 80px;
	}
	/* 相同代码，可以组件化 */
	.guide_bg{
		height: 54px;width: 100%;background-color: #FFFFFF;
	}
	.guide_body_img1{
		position:relative;left: 17px;top: 7px;z-index: 9999;width: 66px;height: 40px;
	}
	.guide_body_img2{
		position:fixed;right: 20px;top: 14px;z-index: 9999;width: 25px;height: 25px;
	}
	.list_cell0{
			width: 88px;
		    height: 32px;
		    margin: 0 auto;
		    color: rgba(33, 32, 32, 1);
		    background-color: rgba(255, 195, 0, 1);
		    border-radius: 16px;
		    font-size: 14px;
		    line-height: 100%;
		    color: #FFFFFF;
	}
	.list_cell1{
		margin-top: 30px;padding-top: 5px;
	}
	.list_cell2{
		margin-top: 30px;
	}
	.wanggougou_login_img{
		background-color: #E7E6E6;padding: 40px 120px;margin-left:calc(50% - 144px);margin-right:calc(50% - 144px);margin-top: 30px;
	}
	.footer_chieseLanguage{
		position: fixed;bottom: 20px;left:calc(50% - 19px);color: rgba(80, 80, 80, 1);
	}
	.text_729X2{
		position: absolute;
		width: 100%;
		height: 36px;
		left: 6px;
		top: 38%;
		letter-spacing: 5px;
		color: rgba(255, 255, 255, 1);
		font-size: 24px;
		line-height: 150%;
		text-align: center;
		font-weight: bold;
	}
	.text_730X2{
		position: absolute;
		width: 100%;
		height: 21px;
		left: 6px;
		top: 52%;
		color: rgba(255, 255, 255, 1);
		font-size: 13px;
		line-height: 150%;
		text-align: center;
	}
	.text_694X2{
		width: 292px;
		height: 99px;
		left: 36px;
		top: 452px;
		color: rgba(80, 80, 80, 1);
		font-size: 10px;
		line-height: 200%;
		text-align: ;
	}
	.social{
		position: relative;
	}
	.text_632X2{
		position: absolute;
		width: 100%;
		height: 19px;
		left: 5px;
		top: 48%;
		color: rgba(106, 109, 108, 1);
		font-size: 13px;
		line-height: 300%;
		text-align: center;
	}
	.social{
		position: relative;
	}
	.text_636X2{
		position: absolute;
		width: 100%;
		height: 50%;
		left: 5px;
		top: 48%;
		color: rgba(255, 255, 255, 1);
		font-size: 13px;
		line-height: 400%;
		text-align: center;
	}
	/deep/.u-indicator-item-round{
	    width: 7px;
	    height: 7px;
	    margin-top: 90px;
	    border-radius: 10px;
	    -webkit-transition: all 0.5s;
	    transition: all 0.5s;
	    background-color: rgba(0, 0, 0, 0.3);
		
	}
	/deep/.u-indicator-item-round-active {
			width: 8px;
	    	height: 8px;
	    	left: 165px;
	    	top: 272px;
	    	color: rgba(80, 80, 80, 1);
	    	background-color: rgba(40, 178, 139, 1);
	    	border-radius: 3px;
	    	font-size: 14px;
	    	line-height: 150%;
	    	text-align: center;
	}
	
	
@import "../../static/css/index";
</style>
