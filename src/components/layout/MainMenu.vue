<template>
	<div class="main-menu noselect">
		<ul>
			<li><span class="hqg icon-panel"></span>我的面板</li>
			<li><span class="hqg icon-shezhi"></span>系统设置</li>
			<li class="active"><span class="hqg icon-content"></span>内容管理</li>
		</ul>
	</div>
</template>

<script>
	export default {

	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.main-menu li{
		height: 40px;
		line-height: 40px;
		cursor: pointer;
	}
	.main-menu li.active{
		background: #31b0d5 !important;	
	}
	.main-menu li:hover{
		background: #44485c;
	}
	.main-menu li.active span,
	.main-menu li:hover span{
		color: #fff;
	}
	.main-menu ul li span{
		width: 50px;
		display: inline-block;
		text-align: center;
		font-size: 14px;
		color: #a6a6a6;
	}
</style>