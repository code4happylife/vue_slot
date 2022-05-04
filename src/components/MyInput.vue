<template>
	<!-- 组件实现v-model属性,1.给组件定义modelValue属性 2.给组件定义update:modelValue事件 -->
	<div class="box">
		这个是myInput组件
		<input type="text" :value="modelValue" @input="updateValue">
<!--		<input type="text" :value="modelValue" @input="$emit('update:modelValue',event.target.value)">-->
	</div>
</template>

<script>
	export default {
		data() {
			return {

			};
		},
		// 给组件定义属性
		props: ['modelValue'],
		//给组件定义事件
		emits: ['update:modelValue'],
		methods: {
			updateValue(event) {
				this.$emit('update:modelValue', event.target.value)
			}
		}
	}
</script>

<style>
	.box {
		width: 200px;
		height: 100px;
		background-color: #42B983;
	}
</style>
