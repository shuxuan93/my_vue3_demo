<template>
	<view class="content">
		<button @click="show">显示</button>
		<input v-if="isShow" focus ref="inputRef" type="text" placeholder="123" />
	</view>
</template>

<script setup>
	import {
		ref,
	} from 'vue';
	import {
		onShow,
		onHide,
		onLoad,
		onPageScroll
	} from "@dcloudio/uni-app";
	const isShow = ref(false)
	const inputRef = ref(null)
	const show = () => {
		isShow.value = true
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>