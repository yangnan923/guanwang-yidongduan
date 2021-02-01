<template>
	<view class="babyLandPage">
		<myHeader style="margin-bottom: 110rpx;"></myHeader>
		<view class="babyLandBg">
			<view class="video_box">
				<video :controls="true" class="myVideo" @play="isPlay=false" @pause="isPlay=true" :autoplay="true" id="myVideo" src="https://wggdown.wanggougou.cn/webimg/video/description.mp4" style="width: 100%; height: 100%;" object-fit="cover"
				 :enable-progress-gesture="true"  poster="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/videoImg.png"></video>
				<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/player.png" class="playerImg" v-show="isPlay" ></image>
			</view>
		</view>
		<view class="appTitle">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/babyTitle1.png" class="babyTitle"></image>
			<view class="appText">
				以“培养宝贝自发学习力”为产品理念，构建涵盖
				学龄前儿童的启蒙课程，数学思维、国学等。
			</view>
			<view class="appText">
				运用AI交互技术，打造寓教于乐的学习场景，实时正向反馈学习行径，结合感官训练，激发孩子探知好奇心。
			</view>
			<view class="appText">
				培养自主学习能力，为其日后的学习建立一个良好的开端与基础。
			</view>
		</view>
		<view class="qrCode">
			<view class="qrCode_item">
				<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/iosOrAn.png" class="iosOrAn"></image>
				<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/downBtn.png" class="downBtn1"></image>
			</view>
			<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/babyLand/QRcode.png" class="qrIcon"></image>
		</view>
		<view class="learningBoard">
			<view class="learningBoard_title">
				<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/babyLand/studyBoard4.png" class="studyBoard"></image>
			</view>
		<!-- 	<view class="learningBoard_pages">
				<view class="pages">
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/teach1.png" class="teach" :class="pageImgIndex==0? 'teachActive':'' "  @click="pageImgIndex=0"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/learn1.png" class="teach" :class="pageImgIndex==1? 'teachActive':''" @click="pageImgIndex=1"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/measure1.png" class="teach" :class="pageImgIndex==2? 'teachActive':''" @click="pageImgIndex=2"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/Practice1.png" class="teach" :class="pageImgIndex==3? 'teachActive':''" @click="pageImgIndex=3"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/review1.png" class="teach" :class="pageImgIndex==4? 'teachActive':''" @click="pageImgIndex=4"></image>
				</view>
			</view>
			<image src="https://wggdown.wanggougou.cn/webimg/pc20201027/product/class.png" class="pageImg" v-show="pageImgIndex==0"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/pc20201027/product/risk.png" class="pageImg" v-show="pageImgIndex==1"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/pc20201027/product/outer.png" class="pageImg" v-show="pageImgIndex==2"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/pc20201027/product/freedom.png" class="pageImg" v-show="pageImgIndex==3"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/pc20201027/product/report.png" class="pageImg" v-show="pageImgIndex==4"></image> -->
			<scroll-view class="scroll-view_H" :scroll-x="true"@scroll="scroll" scroll-left=24 >
				<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/babyLandt.png" class="scroll-view-item_H"></image>
			</scroll-view>
		</view>
		<view class="scienceBg">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/scienceTitle.png" class="scienceTitle"></image>
		</view>
		<view class="yeBg">
			<view class="bgTitle">
				寓教于乐
			</view>
			<view class="bgTxet">
				以娱教方式主动获取知识，激发儿童求知好奇心，培养儿童自主学习力。
			</view>
		</view>
		<view class="redBg">
			<view class="bgTitle">
				衔接幼小
			</view>
			<view class="bgTxet">
				开发孩子的全方位潜能，实现幼升小顺利过渡。
			</view>
		</view>
		<view class="ziBg">
			<view class="bgTitle">
				思维提升
			</view>
			<view class="bgTxet">
				鼓励孩子以思维能力探索，培养全科思维意识。
			</view>
		</view>
		<view class="san">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/ThreeEngineer1.png" class="ThreeEngineer"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/expert1.png" class="expert"></image>
			<image src="https://wggdown.wanggougou.cn/webimg/wap20210108/babyLand/curriculum3.png" class="curriculum"></image>
		</view>
		<!-- <view class="footerBg">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/lovelearning.png" class="lovelearning"></image>
			<view class="qrCode" style="padding: 0 66rpx;">
				<view class="qrCode_item">
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/iosOrAn.png" class="iosOrAn"></image>
					<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/downBtn.png" class="downBtn"></image>
				</view>
				<image src="https://wggdown.wanggougou.cn/webimg/pc20201212/index/downMarych.png" class="qrIcon"></image>
			</view>
		</view> -->
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
				pageImgIndex:0,
				isPlay:true
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
	.babyLandPage{
		background: #F5F8FA;
	}
	.babyLandBg{
		width: 750rpx;
		height: 630rpx;
		background-image: url("https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/babyLandBg.png");
		background-size: 100%;
		position: relative;
	}
	.video_box{
		position: absolute;
		width: 682rpx;
		height: 322rpx;
		background-image: url("https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/videoImg.png");
		background-size: 100%;
		left: 50%;
		transform: translateX(-50%);  
		bottom: 46rpx;
		z-index: 0;
	}
	.playerImg{
		width: 196rpx;
		height: 196rpx;
		 position: absolute; left: 50%; top: 50%;
		 transform: translate(-52%, -56%);    /* 50%为自身尺寸的一半 */
	}
	/deep/.uni-video-cover-play-button{
		
		background-color: rgba(25,25,25,0);
		color: rgba(25,25,25,0);
	}
	.appTitle{
		padding: 0 40rpx;
	}
	.babyTitle{
		width: 572rpx;
		height: 148rpx;
		margin: 40rpx 0;
	}
	.appText{
		width: 660rpx;
		font-size: 28rpx;
		font-family: Source Han Sans CN;
		font-weight: 400;
		line-height: 48rpx;
		color: #333333;
	}
	.qrCode{
		padding: 0 40rpx;
		display: flex;
		justify-content: space-between;
		margin: 60rpx 0;
	}
	.qrCode_item{
		width: 45%;
	}
	.iosOrAn{
		width: 296rpx;
		height: 44rpx;
		margin-top: 20rpx;
		margin-bottom: 52rpx;
	}
	.downBtn1{
		width: 302rpx;
		height: 88rpx;
		background-color: #D97B00;
		box-shadow: 0px 6px 12px rgba(217, 123, 0, 0.37);
		border-radius: 38px;
	}
	.qrIcon{
		width: 220rpx;
		height: 220rpx;
	}
	.learningBoard{
		position: relative;
	}
	.learningBoard_title{
		height: 192rpx;
		opacity: 1;
		padding-top: 54rpx;
	}
	.studyBoard{
		display: block;
		margin: 0 auto;
		width: 756rpx;
		height: 100rpx;
	}
	.learningBoard_pages{
		height: 872rpx;
		background: #D6EEFF;
		opacity: 1;
		
	}
	.pages{
		padding: 20rpx;
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
		position: absolute;
		bottom: 0rpx;
	}
	.teach{
		width: 226rpx;
		height: 226rpx;
		opacity:0.5;
	}
	.teachActive{
		opacity:1;
	}
	.pageImg{
		width: 670rpx;
		height: 488rpx;
		box-shadow: 0px 30px 60px rgba(4, 73, 151, 0.2);
		position: absolute; left: 50%; top: 204rpx;
		transform: translateX(-50%) ;   /* 50%为自身尺寸的一半 */
	}
	.scienceBg{
		width: 750rpx;
		height: 700rpx;
		background-image:url("https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/scienceBg.png") ;
		background-size: 100%;
	}
	.scienceTitle{
		display: block;
		margin: 0 auto;
		padding-top: 38rpx;
		width: 692rpx;
		height: 100rpx;
	}
	.yeBg,.redBg,.ziBg{ width: 670rpx; height: 598rpx; margin: 0 auto; margin-bottom: 26rpx;position: relative;}
	.yeBg{
		background-image:url("https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/yeBg.png") ;
		background-size: 100%;
		}
	.redBg{
		background-image:url("https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/redBg.png") ;
		background-size: 100%;
		}
	.ziBg{
		background-image:url("https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/ziBg.png") ;
		background-size: 100%;
		}
	.bgTitle{
		height: 52rpx;
		font-size: 52rpx;
		font-family: Source Han Sans CN;
		font-weight: 800;
		line-height: 44px;
		color: #707070;
		opacity: 1;
		position: absolute; left: 50%; top: 228rpx;
		    transform: translateX(-50%);
	}
	.bgTxet{
		width: 468rpx;
		height: 134rpx;
		font-size: 32rpx;
		font-family: Source Han Sans CN;
		font-weight: 400;
		line-height: 48rpx;
		text-align: center;
		color: #707070;
		opacity: 1;
		position: absolute; left: 50%; top: 334rpx;
		transform: translateX(-50%);
	}
	.san{
		padding-top: 32rpx;
	}
	.ThreeEngineer{
		width: 750rpx;
		height: 816rpx;
	}
	.expert{
		display: block;
		width: 670rpx;
		height: 816rpx;
		margin: 0 auto;
		margin-top: 76rpx;
	}
	.curriculum{
		display: block;
		width: 670rpx;
		height: 770rpx;
		margin: 0 auto;
		margin-top: 60rpx;
	}
	.footerBg{
		width: 750rpx;
		height: 708rpx;
		background-image:url("https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/footerBg.png") ;				background-size: 100%;
				padding-top: 44rpx;
				margin-top: 33px;
	}
	.lovelearning{
		width: 320rpx;
		height: 40rpx;
		display: block;
		margin: 0 auto;
	}
	// 横向
	.scroll-view_H {
		white-space: nowrap;
		width: 100%;
	}
	// 横向
	.scroll-view-item_H {
		display: inline-block;
		width: 2914rpx;
		height: 870rpx;
	}
	.footer_box{
		background-image: url("https://wggdown.wanggougou.cn/webimg/wap20210108/babyLand/footer3.png");
		background-repeat: no-repeat;
		background-size: 100%;
		width: 750rpx;
		height: 808rpx;
		position: relative;
		margin-top: -120rpx;
	}
	.downBtn{
		width: 254rpx;
		height: 70rpx;
		position: absolute;
		left: 148rpx;
		bottom: 224rpx;
	}
</style>
