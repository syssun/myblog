<template>
	<div class="home">
		<el-row id="artList" type="flex" justify="space-around">
			<el-col :span="4" class="hidden-sm-and-down" id="leftsSide">
				<div class="item">
					<tag></tag>
				</div>
				
			</el-col>
			<el-col :span="12">
				<el-row class="art-item">
					<router-link to="/article" tag="span">
					<el-card shadow="hover">
						<h5><img src="../assets/star.png" style="width: 1.25rem;height: 1.25rem;" />          这是标题啊啊啊啊啊啊啊啊</h5>
						<el-row class="art-body">
							<div class="side-img hidden-sm-and-down">
								<img class="art-banner" src="../assets/vue.jpg">
							</div>
							<div class="side-abstract">
								<div class="art-abstract">
									Iconfont-国内功能很强大且图标内容很丰富的矢量图标库, 提供矢量图标下载、在快照 在小程序中使用阿里文字图标在小程序中使用阿里文字图标库前在小程序中使用阿里文字图标库前库前端开发...
								</div>
							</div>
						</el-row>
					</el-card>
					</router-link>
				</el-row>
				<div class="block pagination">
					<el-pagination background="#f9f9f9" layout="prev, pager, next" :total="50">
					</el-pagination>
				</div>
			</el-col>
			<el-col :span="6" class="hidden-sm-and-down" id="side">
				<div class="item">
					<tag></tag>
				</div>
				<div class="item">
					<friend></friend>
				</div>
			</el-col>
		</el-row>

	</div>
</template>

<script>
	import friend from '../components/friend'
	import tag from '../components/tag'
	export default {
		name: 'home',
		components: {
			friend,
			tag
		}
	}
</script>

<style scoped>
	#side .item {
		margin-bottom: 30px;
	}
	
	.art-item {
		margin-bottom: 30px;
		position: relative;
		cursor: pointer;
	}
	
	.art-item .star {
		width: 60px;
		height: 60px;
		position: absolute;
		top: 0;
		right: 0;
	}
	
	img.tag {
		width: 16px;
		height: 16px;
	}
	
	.art-title {
		border-left: 3px solid #F56C6C;
		padding-left: 5px;
		cursor: pointer;
	}
	
	.art-title:hover {
		padding-left: 10px;
		color: #409EFF;
	}
	
	.art-time {
		margin-right: 20px;
	}
	
	.art-body {
		display: flex;
		padding: 10px 0;
	}
	
	.side-img {
		height: 60px;
		width: 100px;
		overflow: hidden;
		margin-right: 10px;
	}
	
	img.art-banner {
		width: 100%;
		height: 100%;
		transition: all 0.6s;
	}
	
	img.art-banner:hover {
		transform: scale(1.4);
	}
	
	.side-abstract {
		flex: 1;
		display: flex;
		flex-direction: column;
	}
	
	.art-abstract {
		flex: 1;
		color: #aaa;
	}
	
	.art-more {
		height: 40px;
		display: flex;
		justify-content: space-between;
		align-items: flex-end;
	}
	
	.art-more .view {
		color: #aaa;
	}
	h5{
		font-size: 18px;
	}
	.pagination {
		background-color: #F9F9F9;
	}
</style>