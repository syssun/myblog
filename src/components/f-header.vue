<template>
	<div>
		<el-menu :default-active="activeIndex" class="d-flex" mode="horizontal" router="true" type="flex">
			<el-menu-item class="mr-auto">
				<router-link  to="/home">
					<img style="width: 30px;height: 30px;" src="../assets/logo.png" />
				</router-link>
				
			</el-menu-item>
			<el-menu-item class="mr-auto" style="cursor: default;">
				<span>签名</span>
			</el-menu-item>
			<el-menu-item >
				<el-input 
					size="small"
					class="sinput"
				    placeholder="请输入内容"
					style="border: none;"
				    >
				</el-input>
			</el-menu-item>
			<el-menu-item index="/home">{{$t("header.home")}}</el-menu-item>
			
			<el-menu-item index="/about">{{$t("header.about")}}</el-menu-item>
			
		</el-menu>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				activeIndex: '/home'
			};
		},
		methods: {
			toggleLang(lang) {
				if(lang === 'zh') {
					localStorage.setItem('locale', 'zh')
					this.$i18n.locale = localStorage.getItem('locale')
					this.$message({
						message: '切换为中文！',
						type: 'success'
					})
				} else if(lang === 'en') {
					localStorage.setItem('locale', 'en')
					this.$i18n.locale = localStorage.getItem('locale')
					this.$message({
						message: 'Switch to English!',
						type: 'success'
					})
				}
			}
		}
	}
</script>

<style scoped>
	input{
		border: none;
	}
  .sinput > input{
	  border: none;
  }
  .el-input--small .el-input__inner {
      height: 32px;
      line-height: 32px;
      border: none;
  }
</style>