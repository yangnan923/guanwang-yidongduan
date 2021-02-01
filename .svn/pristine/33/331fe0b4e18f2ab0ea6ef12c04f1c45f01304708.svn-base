<template>
	<view class="headerPage">
		<view :style="style" id="guide_header" >
							 
							  <img class="wanggougou_header_img" src="https://wggdown.wanggougou.cn/webimg/wap20201014/header.png" >
							   <img v-if = "menu == 2" class="guide_header_img1"  src="../../static/index/goMenu.gif" @click="showPopup(0)" >
							  <img v-if = "menu == 0" class="guide_header_img1"  src="../../static/index/outMenu.gif" @click="showPopup(2)" >
		</view>
		<!-- #ifdef MP-WEIXIN -->
		<u-popup v-model="show" mode="top" width="100%" height="230px">
			<!-- <view style="height: 50px;"></view> -->
		<!-- #endif -->
		<!-- #ifdef H5 -->
		<u-popup v-model="show" mode="top" width="100%" height="100%">
		<!-- #endif -->
			<view class="guide_bg">
			  <!-- <img class="guide_body_img1" src="https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/icon.png" alt=""> -->
			  <!-- <img class="guide_body_img2"  src="https://wggdown.wanggougou.cn/webimg/wap20200911/static/index/menu_green.png" @click="showPopup" alt=""> -->
			</view>
			<view class="icon_106X2"></view>
			<view :class="isactive==1?'list_celll0':''" class="list-cell memu-text " @click="openUrl(1)">
				<text>
					首页
				</text>
			</view>
			<view :class="isactive==2||isactive==5||isactive==6||isactive==7?'list_celll1':''" class="list-cell memu-text list_cell1"  @click="showProduct(2)">
				<text>线上产品</text>
				<img v-if="isshow_product" class="icon_103X2" src="../../static/index/arrow_down_white.svg">
				<!-- <img  class="icon_103X2" src="../../static/index/arrow_down.svg" alt=""> -->
			</view>
				<view v-show="isshow_product" class="wanggougou_login_img" >
					<view class="img_box">
						<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/clickSafe.png" class="pageImg"  @click="openUrl(6)"></image>
					</view>
					<view class="img_box">
						<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/clickGame.png" class="pageImg" @click="openUrl(2)"></image>
					</view>
					<view class="img_box">
						<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/guide/clickHome.png" class="pageImg" @click="openUrl(5)"></image>
					</view>
					<view class="img_box">
						<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/childrenStyle/childrenStyle.png" class="pageImg" @click="openUrl(7)"></image>
					</view>
				</view>
			<view :class="isactive==3?'list_celll1':''" class="list-cell memu-text" style="margin-top: 30px;" @click="openUrl(3)">
				关于我们
			</view>
			<view :class="isactive==4?'list_celll2':''"  class="list-cell memu-text list_cell2"  @click="openUrl(4)">
				招商加盟
			</view>
			<!-- <view   class="footer_chieseLanguage" @click="openUrl(1)">
				中文版
			</view> -->
		</u-popup>
	</view>
	
</template>

<script>
	export default {
		data() {
			return {
				show: false,
				style: {},
				menu:0, //分类按钮状态
				isshow_product:false,
				isactive:1,
			}
		},
		
		created() {
			this.isactive = uni.getStorageSync('key');
		},
		beforeDestroy(){
		       // 初始化保存数据到本地,选中导航是第1个
		        // const info = 1;
		        //    uni.setStorageSync('key', info);
		},　
		methods: {
			showPopup(index){
				// this.isshow_product = false
				this.menu=index
				
				this.isactive =  uni.getStorageSync('key');
				if(this.show){
					this.show =false
				}else{
					this.show =true
				}
			},
			showProduct(index){
				this.isactive=index
				if(this.isshow_product){
					this.isshow_product = false
				}else{
					this.isshow_product = true
				}
			},
			scroll(event) {
							//距离每个边界距离
					console.log(event.detail)
			},
			openUrl(index){
				this.show =false
				// 保存数据到本地
				 const info = index;
				     uni.setStorageSync('key', info);
					// this.isactive=index
				if(index == 1){
					uni.redirectTo({
						url:"../../pages/index/guide"
					})
					
				}else if(index == 2){
					uni.redirectTo({
						url:"../../pages/index/babyLand"
					})
					
				}
				else if(index == 4){
					uni.redirectTo({
						url:"../../pages/index/investment"
					})
					
				}
				else if(index==5){
					uni.redirectTo({
						url:"../../pages/index/college"
					})
				}
				else if(index==6){
					uni.redirectTo({
						url:"../../pages/index/security"
					})
				}
				else if(index == 3){
					uni.redirectTo({
						url:"../../pages/index/index"
					})
					
				}
				else if(index == 7){
					uni.redirectTo({
						url:"../../pages/index/childrenStyle"
					})
					
				}
			},
			
		}
	}
</script>

<style>
.icon_106X2{
		width: 24px;
		height: 24px;
		left: calc(100% - 50px);
		top: 0px;
		font-size: 24px;
		color: rgba(153, 153, 153, 1);
		position: relative;
	}
	.ischecked{
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
		.goMenu{
			width: 32rpx;
			height: 32rpx;
		}
	#guide_header{
		 height: 100rpx;
		 position:fixed;
		 top: 0px;
		 left: 0px;
		 z-index: 999999;
		 width: 100%;
		 /* background-color: #FFFFFF; */
		 backdrop-filter: saturate(180%) blur(20px);
		 background-color: rgba(255,255,255,0.72);
		/* background-color: var(--header-background); */
	}
	#guide_header>.guide_header_img1{
		position:fixed;right: 23px;top: 14px;z-index: 9999;
		width: 20px !important;
		height: 20px !important;
	}
	#guide_header>.guide_header_img2{
		position:fixed;left: 46rpx;top: 28rpx;z-index: 9999;width: 50rpx;height: 50rpx;
	}
	 .wanggougou_header_img{
		position:fixed;left: 46rpx;top: 24rpx;z-index: 9999;width: 292rpx;height: 52rpx;
	}
	.guide_bodyImg_height{
		height: 54px;
	}
	.guide_bg{
		height: 54px;width: 100%;background-color: #FFFFFF;
	}
	.guide_body_img1{
		position:relative;left: 17px;top: 7px;z-index: 9999;width: 66px;height: 40px;
	}
	.guide_body_img2{
		position:fixed;right: 20px;top: 14px;z-index: 9999;width: 25px;height: 25px;
	}
	
	.list_celll0{
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
	.list_cell1{
		margin: 0 auto;
		margin-top: 30px;padding-top: 8px;
		padding-right: 8px;
	}
	.list_celll1{
		width: 158px;
		height: 32px;
		margin: 0 auto;
		color: rgba(33, 32, 32, 1);
		background-color: rgba(255, 195, 0, 1);
		border-radius: 16px;
		font-size: 14px;
		color: #FFFFFF;
		margin-top: 30px;padding-top: 6px;
	}
	.list_celll2{
		width: 158px;
		height: 32px;
		margin: 0 auto;
		color: rgba(33, 32, 32, 1);
		background-color: rgba(255, 195, 0, 1);
		border-radius: 16px;
		font-size: 14px;
		color: #FFFFFF;
		margin-top: 30px;
	}
	.list_cell2{
		margin-top: 30px;
	}
	.wanggougou_login_img{
		width: 670rpx;
		height: 560rpx;
		margin: 0 auto;
		margin-top: 16rpx;
		padding: 24rpx 60rpx;
		background: #F8F8F8;
		opacity: 1;
		border-radius: 40rpx;
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		justify-items: center;
	}
	.img_box{
		width: 240rpx;height: 240rpx;
	}
	.pageImg{
		display: block;
		width: 240rpx;height: 240rpx;
		margin: 0rpx auto;
	}
	.footer_chieseLanguage{
		position: fixed;bottom: 20px;left:calc(50% - 19px);color: rgba(80, 80, 80, 1);
	}
	
</style>
