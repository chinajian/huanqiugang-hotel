<template>
	<div class="header noselect">
		<nav class="navbar navbar-default navbar-inverse">
			<div class="container-fluid">
				<div class="navbar-header">
					<button class="navbar-toggle collapsed" type="button" data-toggle="collapse" data-target=".bs-example-js-navbar-collapse">
					<span class="sr-only">Toggle navigation</span>
					<span class="icon-bar"></span>
					<span class="icon-bar"></span>
					<span class="icon-bar"></span>
					</button>
					<a class="navbar-brand hqg icon-logo" href="#"></a>
				</div>
				<div class="collapse navbar-collapse bs-example-js-navbar-collapse">
					<ul class="nav navbar-nav">
						<li class="dropdown">
							<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
							管理控制台
							</a>
						</li>
<!-- 						<li class="dropdown">
							<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
							Dropdown
							<span class="caret"></span>
							</a>
							<ul class="dropdown-menu" aria-labelledby="drop2">
								<li><a href="#">Action</a></li>
								<li role="separator" class="divider"></li>
								<li><a href="#">Separated link</a></li>
							</ul>
						</li> -->
					</ul>
					<ul class="nav navbar-nav navbar-right">
						<li class="dropdown">
							<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
							admin
							<span class="caret"></span>
							</a>
							<ul class="dropdown-menu" aria-labelledby="drop3">
								<li><a href="#">修改密码</a></li>
								<li role="separator" class="divider"></li>
								<li><a href="#">退出</a></li>
							</ul>
						</li>
					</ul>
				</div>
			</div>
		</nav>
	</div>
</template>

<script>
	import jQuery from "jquery"
	import 'bootstrap/dist/css/bootstrap.min.css'
	import 'bootstrap/dist/js/bootstrap.min.js'
	export default {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/*重写bootstarp的样式>>>*/
	/*整个head组件的外围样式*/
	.navbar {
	    border-radius: 0px;
	    margin-bottom: 20px;
    	border: 0px;
	}
	/*一级菜单的链接颜色改为白色*/
	.navbar-inverse .navbar-nav>li>a{
		color: #fff;
	}
	/*LOGO*/
	.navbar-brand{
		color: #b3a36b;
		font-size: 30px;
		padding: 15px 10px 10px 10px;
		background: #32373b;
	}
/*重写bootstarp的样式<<<*/
</style>