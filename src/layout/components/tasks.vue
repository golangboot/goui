<template>
	<scTable ref="table" :apiObj="apiObj" row-key="id" empty-text="没有正在执行的任务" paginationLayout="total, prev, pager, next">
		<sc-table-column label="序号" type="index"></sc-table-column>
		<sc-table-column label="任务名称" prop="taskName" min-width="100"></sc-table-column>
		<sc-table-column label="创建时间" prop="createDate" width="170"></sc-table-column>
		<sc-table-column label="状态" prop="stateName" width="80"></sc-table-column>
		<sc-table-column label="结果" prop="result" width="80">
			<template #default="scope">
				<el-button v-if="scope.row.state=='1'" type="primary" icon="el-icon-download" circle plain size="small" @click="download(scope.row)"></el-button>
			</template>
		</sc-table-column>
	</scTable>
</template>

<script>
	export default {
		data() {
			return {
				apiObj: this.$API.system.tasks.list,
			}
		},
		mounted() {

		},
		methods: {
			download(row){
				let a = document.createElement("a")
				a.style = "display: none"
				a.target = "_blank"
				a.href = row.result
				document.body.appendChild(a)
				a.click()
				document.body.removeChild(a)
			}
		}
	}
</script>

<style scoped>

</style>
