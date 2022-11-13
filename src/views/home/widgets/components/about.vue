<template>
	<el-card shadow="hover" header="关于项目" class="item-background">
		<p>高性能 / 精致 / 优雅。基于Vue3 + Element-Plus 的中后台前端解决方案，如果喜欢就点个星星支持一下。</p>
		<p style="display: flex;align-items: start;align-items: self-start;">
			<a href='https://gitee.com/hungyuvip/bmwboot-ui' target="_blank" style="display: flex;">
				<img src='https://gitee.com/hungyuvip/bmwboot-ui/badge/star.svg?theme=dark' alt='star'>
			</a>
			<a href='https://github.com/hongyukeji/bmwboot-ui' target="_blank" style="display: flex;">
				<img src='https://img.shields.io/github/stars/hongyukeji/bmwboot-ui.svg?style=flat-square&logo=GitHub' alt='star'>
			</a>
		</p>
	</el-card>
</template>

<script>
	export default {
		title: "关于项目",
		icon: "el-icon-setting",
		description: "点个星星支持一下",
		data() {
			return {

			}
		}
	}
</script>

<style scoped>
	.item-background p {color: #999;margin-top:10px;line-height: 1.8;}
</style>
