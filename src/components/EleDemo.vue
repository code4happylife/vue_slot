<template>
  <el-table :data="tableData" style="width: 100%" border size="small">
    <el-table-column type="expand">展开的内容</el-table-column>
    <el-table-column label="序号" type="index" min-width="180"></el-table-column>
    <el-table-column label="日期" prop="date" min-width="180"></el-table-column>
    <el-table-column label="名字" prop="name" min-width="100"></el-table-column>
    <el-table-column label="地址" prop="address" min-width="180"></el-table-column>
    <el-table-column label="操作" min-width="200">
      <template #default="">
        <el-button size="small"  type="primary">编辑</el-button>
        <el-button size="small" type="danger">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
	export default {
		data() {
			return {
				tableData: [{
						date: '2016-05-03',
						name: 'Tom',
						address: 'No. 189, Grove St, Los Angeles',
					},
					{
						date: '2016-05-02',
						name: 'Tom',
						address: 'No. 189, Grove St, Los Angeles',
					},
					{
						date: '2016-05-04',
						name: 'Tom',
						address: 'No. 189, Grove St, Los Angeles',
					},
					{
						date: '2016-05-01',
						name: 'Tom',
						address: 'No. 189, Grove St, Los Angeles',
					},
				]
			};
		}
	};
</script>

<style>
</style>
