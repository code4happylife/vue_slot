<template>
	<div class="login_box">
		<el-form :model="form" label-width="120px">
			<el-form-item label="用户名">
				<el-input v-model="form.name" />
			</el-form-item>
			<el-form-item label="密码">
				<el-input v-model="form.pwd" />
			</el-form-item>
			<el-form-item>
				<el-button type="primary" @click="onSubmit">登录</el-button>
				<el-button>取消</el-button>
			</el-form-item>
		</el-form>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				form: {
					name: "",
					pwd: ""
				}
			}
		},
		methods: {
			onSubmit() {
				console.log('login success!')
			}
		}

	}
</script>

<style>
	.login_box {
		width: 600px;
		height: 400px;
		margin: 200px 0;
		background-color: #42B983;
	}
</style>
