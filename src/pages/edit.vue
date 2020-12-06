<template>
  <div class="container">
	  <el-row :gutter="20">
	    <el-col :span="24">
			<div style="border: 1px solid #409EFF;margin: 10px 0;">
				标题 标签 提交
			</div>
		</el-col>
	    <el-col :span="24">
			<mavon-editor v-model="content" :ishljs="true" :save="save"/>
		</el-col>
	    
	  </el-row>
    
  </div>
  
</template>

<script>
export default {
  name: 'mdEditor',
  data () {
    return {
      content: ''
    }
  },
  methods:{
	  save(){
		  console.log(this.content)
	  }
  }
}
</script>
<style scoped>
	.container{
		width: 100%;
		height: 100%;
	}
</style>