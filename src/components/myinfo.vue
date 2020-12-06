<template>
	<div class="myinfo">
		<el-card class="box-card">
			<div slot="header" class="car-header" style="padding: 0;">
				<img class="card-icon" src="../assets/vue.jpg" />
				<h6>君子不器</h6>
			</div>
			<div class="text item">
				<p>不到最后，焉知生死！</p>
			</div>
		</el-card>
	</div>
</template>

<script>
	export default {
		name: 'myinfo',
		methods: {
			tag(name) {
				this.$router.push({
					name: 'myinfo',
					params: {
						'name': name
					}
				});
			}
		}
	}
</script>

<style scoped>

	.box-card .car-header:hover {
		color: #409EFF;
		cursor: pointer;
	}
	.box-card .car-header,.text {
		padding: 10px;
		justify-content: center;
		justify-items: center;
		justify-self: center;
		text-align: center;
	}
	.box-card span {
		font-weight: bold;
	}
	
	.card-icon {
		width: 80px;
		height: 80px;
		border-radius: 80px;
		justify-content: center;
		justify-items: center;
		justify-self: center;
	}
	
	.tag-item {
		margin-right: 10px;
	}
	
	img.card-icon {
		width: 80px;
		height: 80px;
		border-radius: 80px;
		justify-content: center;
		justify-items: center;
		justify-self: center;
		transition: all 0.6s;
	}
	
	img.card-icon:hover {
		margin-bottom: 16px;
		margin-top: 10px;
		transform: scale(1.2);
	}
	
	
</style>