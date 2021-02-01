<template>
	<view >
		<myHeader style="margin-bottom: 110rpx;"></myHeader>
		<view class="securityPage">
			<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/securityTitle1.png" class="securityTitle"></image>
			<!-- <view class="securityText">
				以爱之名守护孩子安全
			</view> -->
			<view class="badge_box">
				<view class="badgeTitle">
					旺狗狗智能校徽
				</view>
				<view class="badgeText" @click="gobadge()">
					了解详情
				</view>
				<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/badgeIcon.png" @click="gobadge()" class="badgeIcon"></image>
			</view>
			<view class="student_box">
				<view class="studentTitle">
					旺狗狗智能学生证
				</view>
				<view class="studentText"  @click="goStudent()">
					了解详情
				</view>
				<image src="https://wggdown.wanggougou.cn/webimg/wap20201212/babyLand/studentIcon.png"  @click="goStudent()" class="studentIcon"></image>
			</view>
		</view>
	</view>	
</template>

<script>
	import myHeader from '@/components/my_header/my_header';
	export default {
		components: { myHeader },
		data() {
			return {
				
			}
		},
		methods: {
			gobadge(){
				uni.redirectTo({
					url:"badge"
				})
			},
			goStudent(){
				uni.redirectTo({
					url:"student"
				})
			}
		}
	}
</script>

<style scoped>
	.securityPage{
		padding: 64rpx 40rpx;
		background: #F5F8FA;
		opacity: 1;
		text-align: center;
	}
	.securityTitle{
		display: block;
		margin: 0 auto;
		width: 504rpx;
		height: 160rpx;
	}
	.securityText{
		height: 32rpx;
		font-size: 32rpx;
		font-family: Source Han Sans CN;
		font-weight: 500;
		line-height: 54rpx;
		color: #707070;
		opacity: 1;
		margin: 20rpx auto;
		padding-bottom: 60rpx;
	}
	.badge_box,.student_box{
		width: 670rpx;
		height: 670rpx;
		margin: 54rpx auto;
		background: #FFFFFF;
		opacity: 1;
		border-radius: 20rpx;
		position: relative;
		
	}
	.badgeTitle,.studentTitle{
		width: 360rpx;
		height: 40rpx;
		font-size: 40rpx;
		font-family: Source Han Sans CN;
		font-weight: bold;
		line-height: 68rpx;
		color: #707070;
		opacity: 1;
		position: absolute;
		top: 52rpx;
		left: 50%;
		transform: translateX(-50%);
	}
	.badgeText,.studentText{
		width: 128rpx;
		height: 32rpx;
		font-size: 32rpx;
		font-family: Source Han Sans CN;
		font-weight: 500;
		line-height: 54rpx;
		color: #FFC300;
		opacity: 1;
		position: absolute;
		top: 124rpx;
		left: 50%;
		transform: translateX(-50%);
	}
	.badgeIcon,.studentIcon{
		width: 510rpx;
		height: 426rpx;
		position: absolute;
		bottom: 2rpx;
		left: 50%;
		transform: translateX(-50%);
	}
	
</style>
