<template>
	<h1>这个是ele-demo的根组件{{name}}</h1>
	<MyInput v-model="name"></MyInput>
	<!-- 组件v-model原理 -->
	<!-- <MyInput :model-value="name" @update:model-value="updateHandle"></MyInput> -->
	<el-divider>
		<h1>python</h1>
	</el-divider>

	<SlotDemo>
		<template v-slot:title>
			这是title
		</template>
		<template #age>
			这是age
		</template>
		<h1>python 你好</h1>
	</SlotDemo>

	<!--  -->
	<DemoShow :datas='datas'>
    <template v-slot:title='tt'>
			相关信息{{tt.age}} -- {{tt.hh}}
		</template>
	</DemoShow>
	<EleDemo></EleDemo>
	<LoginBox></LoginBox>
	<h1>ook</h1>

</template>

<script>
	import MyInput from './components/MyInput.vue'
	import DemoShow from './components/DemoShow.vue'
	import EleDemo from './components/EleDemo.vue'
	import LoginBox from './components/LoginBox.vue'
  import SlotDemo from './components/SlotDemo.vue'

  export default {
		name: 'App',
		data() {
			return {
				name: "testuser",
				datas: [{
						id: 1,
						name: '用例1'
					},
					{
						id: 2,
						name: '用例2'
					},
					{
						id: 3,
						name: '用例3'
					},
				],
			}
		},
		components: {
			MyInput,
			SlotDemo,
			DemoShow,
			EleDemo,
			LoginBox
		},
		methods: {
			updateHandle(value) {
				this.name = value
			}
		}
	}
</script>

<style>

</style>
