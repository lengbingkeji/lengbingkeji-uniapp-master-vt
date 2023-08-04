<template>
	<view>
		<scroll-view :scroll-y="modalName==null" class="page" :class="modalName!=null?'show':''">
			<cu-custom bgColor="bg-gradual-pink" :isBack="true">
				<block slot="content">诗歌列表</block>
			</cu-custom>
			<view style="display: flex;">
				<tui-nodata imgWidth="500" imgHeight="400" img-url="https://img.wenhairu.com/images/2023/08/02/7notX.png">
					<view>诗歌列表，开发中...</view>
				</tui-nodata>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	import tuiNodata from "@/components/thorui/tui-no-data/tui-no-data"
	export default{
		data(){
			return{
				modalName: null,
				item:{msg:'退出成功'},
				plan_type,
				type:"1",
				selected:[],
				beginTime:''
			}
		},
		methods:{
			
		},
		components:{
			tuiNodata,
		}
	}
</script>

<style>
</style>