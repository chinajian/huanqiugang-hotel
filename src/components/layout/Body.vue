<template>
	<div class="body">
		<!-- 主菜单 -->
		<div class="main-menu" :class="mainMenuStatus?'hide-main-menu':'show-main-menu'">
			<div class="fold-btn hqg icon-menu" @click='toggleMainMenu'></div><!-- 关闭 主菜单 -->
			<main-menu></main-menu>
		</div>
		<!-- 副菜单 -->
		<div class="sub-menu" :class="subMenuStatus?'hide-sub-menu':'show-sub-menu'">
			<div class="fold-sub-btn hqg icon-lachu" @click='toggleSubMenu' v-show='!subMenuStatus'></div><!-- 关闭 副导航 -->
			<sub-menu></sub-menu>
		</div>
		<!-- 内容 -->
		<div class="content">
			<div class="fold-sub-btn hqg icon-lachu" @click='toggleSubMenu' v-show='subMenuStatus'></div><!-- 显示 副菜单 -->
			11111111111111
		</div>
	</div>
</template>

<script>
	import MainMenu from 'components/layout/MainMenu'//主菜单
	import SubMenu from 'components/layout/SubMenu'//副菜单
	export default {
		components: {
            MainMenu,
            SubMenu
        },
        data(){
            return {
            	mainMenuStatus: false,//主菜单折叠状态
            	subMenuStatus: false//副菜单折叠状态
            }
        },
        methods:{
        	/*主菜单折叠*/
            toggleMainMenu: function(){
            	if(!this.mainMenuStatus){
                	this.mainMenuStatus = true;
            	}else{
                	this.mainMenuStatus = false;            		
            	}
            },
        	/*副菜单折叠*/
            toggleSubMenu: function(){
            	if(!this.subMenuStatus){
                	this.subMenuStatus = true;
            	}else{
                	this.subMenuStatus = false;            		
            	}
            }
        }
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.body{
		height: 100%;
		display: flex;
		position: relative;
	}
	/*主菜单 B*/
	.main-menu{
		width: 160px;
		background: #101010;
		color: #fff;
		overflow: hidden;
	}
	.main-menu.hide-main-menu{
	    animation: hide-main-menu 200ms ease 1 forwards;
		-moz-animation: hide-main-menu 200ms ease 1 forwards;
		-webkit-animation: hide-main-menu 200ms ease 1 forwards;
		-o-animation: hide-main-menu 200ms ease 1 forwards;
	}
	.main-menu.show-main-menu{
	    animation: show-main-menu 200ms ease 1 forwards;
		-moz-animation: show-main-menu 200ms ease 1 forwards;
		-webkit-animation: show-main-menu 200ms ease 1 forwards;
		-o-animation: show-main-menu 200ms ease 1 forwards;
	}
	.main-menu .fold-btn{
		line-height: 30px;
		text-align: center;
		background: #37424f;
		cursor: pointer;
		font-size: 20px;
	}
	.main-menu.show-main-menu .fold-btn::before{
		display: inline-block;
		transform: rotate(90deg);
	}
	/*隐藏菜单 主菜单*/
	@keyframes hide-main-menu{
		to {width: 50px;}
	}
	@-moz-keyframes hide-main-menu{
		to {width: 50px;}
	}
	@-webkit-keyframes hide-main-menu{
		to {width: 50px;}
	}
	@-o-keyframes hide-main-menu{
		to {width: 50px;}
	}
	/*显示菜单 主菜单*/
	@keyframes show-main-menu{
		from {width: 50px;}
		to {width: 160px;}
	}
	@-moz-keyframes show-main-menu{
		from {width: 50px;}
		to {width: 160px;}
	}
	@-webkit-keyframes show-main-menu{
		from {width: 50px;}
		to {width: 160px;}
	}
	@-o-keyframes show-main-menu{
		from {width: 50px;}
		to {width: 160px;}
	}
	/*主菜单 E*/
	
	/*副菜单 B*/
	.fold-sub-btn{
		width: 20px;
		height: 50px;
		cursor: pointer;
		position: absolute;
		top: 50%;
		transform: translateY(-25px);
		border-top: 9px solid transparent;
	    border-left: none;
	    border-right: 20px solid #f7f7f7;
	    border-bottom: 9px solid transparent;
	}
	.fold-sub-btn::before{
		position: absolute;
		top: 50%;
		right: -20px;
		transform: translateY(-10px);
	}
	.sub-menu{
		width: 160px;
		background: #e8ebef;
		position: relative;
		overflow: hidden;
	}
	.sub-menu.hide-sub-menu{
	    animation: hide-sub-menu 200ms ease 1 forwards;
		-moz-animation: hide-sub-menu 200ms ease 1 forwards;
		-webkit-animation: hide-sub-menu 200ms ease 1 forwards;
		-o-animation: hide-sub-menu 200ms ease 1 forwards;
	}
	.sub-menu.show-sub-menu{
	    animation: show-sub-menu 200ms ease 1 forwards;
		-moz-animation: show-sub-menu 200ms ease 1 forwards;
		-webkit-animation: show-sub-menu 200ms ease 1 forwards;
		-o-animation: show-sub-menu 200ms ease 1 forwards;
	}
	.sub-menu .fold-sub-btn{
		z-index: 1;
		right: -6px;
	    transition: all 100ms ease-out 0s;
	}
	.sub-menu .fold-sub-btn:hover{
	    right: 0px;
	}
	/*隐藏菜单 副菜单*/
	@keyframes hide-sub-menu{
		to {width: 0px;}
	}
	@-moz-keyframes hide-sub-menu{
		to {width: 0px;}
	}
	@-webkit-keyframes hide-sub-menu{
		to {width: 0px;}
	}
	@-o-keyframes hide-sub-menu{
		to {width: 0px;}
	}
	/*显示菜单 副菜单*/
	@keyframes show-sub-menu{
		from {width: 0px;}
		to {width: 160px;}
	}
	@-moz-keyframes show-sub-menu{
		from {width: 0px;}
		to {width: 160px;}
	}
	@-webkit-keyframes show-sub-menu{
		from {width: 0px;}
		to {width: 160px;}
	}
	@-o-keyframes show-sub-menu{
		from {width: 0px;}
		to {width: 160px;}
	}
	/*副菜单 E*/

	/*内容 B*/
	.content .fold-sub-btn{/*显示  副菜单*/
		display: inline-block;
		border-right: 20px solid #d5dae1;
		transform: translateY(-25px) rotate(180deg);
		transform-origin: center center;
		position: absolute;
		left: -6px;
		transition: all 100ms ease-out 0s;
	}
	.content .fold-sub-btn:hover{
	    left: 0px;
	}

	.content{
		flex: 1;
		height: 100%;
		position: relative;
		overflow: hidden;
	}
	/*内容 E*/

</style>