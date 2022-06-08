<template>
	<view>
		<!-- 轮播图 -->
		<u-swiper :list="imgList"></u-swiper>
		<!-- 标签 -->
		<u-tabs class='u-margin-top-20' bar-width="100" :list="sortList" :is-scroll="false" :current="currentSort" @change="change"></u-tabs>
		
		<view class="wrap">
			<u-row gutter="16">
				<u-col span="6" v-for="i in 12">	
						<navigator url="#" class="goods-item">
								<u-image width="100%" height="350rpx" src="https://oss.shop.eduwork.cn/ad/2020-0820-5f3dfe9530bfd.png"></u-image>
								<view class="title">区块链</view>
								<view class="u-flex u-row-between">
									<view class="price">￥ 99</view>
									<view class="sales">销量：10</view>
								</view>
						</navigator>
				</u-col>
				
			</u-row>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgList: [
					'https://cdn.uviewui.com/uview/swiper/1.jpg',
					'https://cdn.uviewui.com/uview/swiper/2.jpg',
					'https://cdn.uviewui.com/uview/swiper/3.jpg',
				],
				sortList: [
					{name: '默认'},
					{name: '销量'},
					{name: '推荐'},
					{name: '最新'},
				],
				currentSort: 0
			}
		},
		methods: {
			change(index) {
				this.currentSort = index;
			}
		}
	}
</script>

<style scoped lang="scss">
.goods-item{
	padding: 40rpx;
	margin-top:30rpx ;
	box-shadow:0 12rpx 20rpx 0 rgba(0,0,0,.1);
	.title{
		margin-top: 20rpx;
		font-weight: 500;
		font-size: 32rpx;
	}
	.price{
		color: red;
	}
	.sales{
		color: #888;
	}
}
</style>