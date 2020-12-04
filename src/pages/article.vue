<template>
	<div>
		<el-row class="main" type="flex" justify="center">
			<el-col :span="16">
				<div id="artcle-info">
					<h2 class="text-center"><strong>Springboot—整合swagger2</strong></h2>
					<!-- 描述：文章信息 -->
					<div class="text-center timeAndView">
						<span class="article-time">
							<i class="el-icon-time"></i>
							发表于：<span>2018-08-02</span>
						</span>
						&nbsp;|&nbsp;
						<span class="article-views">
							<i class="el-icon-view"></i>
							阅读量：<span>1</span>w
						</span>
					</div>
					
				</div>
				<hr />
				<div id="artcle-content">
					这里是个富文本
				</div>
				<div id="statement">
					<i>
						天生我材必有用，千金散尽还复来
					</i>
					
				</div>
			</el-col>
		</el-row>
	</div>
</template>

<script>
	export default {
		name: 'article'
	}
</script>

<style scoped>
	#artcle-info {
		padding: 10px;
		margin-bottom: 10px;
	}
	
	#artcle-info .abstract {
		border-left: 3px solid #F56C6C;
		padding: 10px;
		background-color: rgba(126, 129, 135, 0.3);
	}
	
	#artcle-info .timeAndView {
		padding: 5px;
		line-height: 5px;
		font-size: 10px;
		color: #AAAAAA;
	}
	
	pre.has {
		background-color: rgba(0, 0, 0, 0.8);
	}
	
	img.has {
		width: 100%;
	}
	#statement {
		padding: 16px;
		background-color: #EBEEF5;
	}
</style>