<script>
	export default {
		onLaunch: function() {
			console.log('App key')
			uni.getSystemInfo({
			    success: function (res) {
					uni.setStorageSync("windowHeight",res.windowHeight)
			        console.log(res.windowHeight);
			    }
			});
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide');
			uni.setStorageSync('key', 1);
		}
	}
</script>

<style lang="scss">
	/* 注意要写在第一行，同时给style标签加入lang="scss"属性 */
	@import "uview-ui/index.scss";
</style>
