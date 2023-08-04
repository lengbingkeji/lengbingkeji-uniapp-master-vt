<template>
	<view>
		<home :cur="PageCur" v-if="PageCur=='home'" :key="commponent1Key"></home>
		<people v-if="PageCur=='people'" :key="commponent2Key"></people>
		<works v-if="PageCur=='works'" :key="commponent3Key"></works>
		<program v-if="PageCur=='program'" :key="commponent3Key"></program>
		<view class="cu-bar tabbar bg-white shadow foot">
			<view :class="PageCur=='home'?'action text-green':'action text-gray'" @click="NavChange" data-cur="home">
				<view class='cuIcon-homefill'></view>主页
			</view>
			<view :class="PageCur=='works'?'action text-green':'action text-gray'" @click="NavChange" data-cur="works">
				<view class='cuIcon-wefill'></view>作品
			</view>
			<view :class="PageCur=='program'?'action text-green':'action text-gray'" @click="NavChange" data-cur="program">
				<view class='cuIcon-writefill'></view>编程
			</view>
			<view :class="PageCur=='people'?'action text-green':'action text-gray'" @click="NavChange" data-cur="people">
				<view class='cuIcon-people'></view>个人
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				PageCur: 'home',
				commponent1Key: 0,
				commponent2Key: 0,
				commponent3Key: 0,
				commponent4Key: 0,
			}
		},
		onLoad:function(){
			this.PageCur='home'
			++this.commponent1Key
			++this.commponent2Key
			++this.commponent3Key
			++this.commponent4Key
		},
		methods: {
			NavChange: function(e) {
				this.PageCur = e.currentTarget.dataset.cur
			}
			
		}
	}
</script>

<style>

</style>
