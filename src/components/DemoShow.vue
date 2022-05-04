<template>
	<div style="background-color: aquamarine; height: 100px;">
		<!-- 作用域插槽 -->
		<slot name="title" :age='age' :hh='haha'></slot>
	</div>

	<table border="1">
		<tr>
			<th>ID</th>
			<th>Name</th>
		</tr>
		<tr v-for='item in datas' :key='item.id'>
      <td>{{item.id}}</td>
      <td>{{item.name}}</td>
    </tr>
	</table>
</template>

<script>
	export default {
		props: ['datas'],
		data() {
			return {
				age: 18,
				haha: "这是哈哈"
			}
		}
	}
</script>

<style>
</style>
