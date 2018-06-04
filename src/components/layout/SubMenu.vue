<template>
	<div class="sub-menu noselect">
		<div class="title">内容管理</div>
		<ul class="menu">
			<li class="down-jiantou" @click='toggleMenu'><span class="hqg icon-biaotou-daoxu"></span>文章管理</li>
			<ul>
				<li class="active">文章分类</li>
				<li>文章列表</li>
			</ul>
			<li class="down-jiantou" @click='toggleMenu'><span class="hqg icon-biaotou-daoxu"></span>文章管理</li>
			<ul>
				<li>文章分类</li>
				<li>文章列表</li>
			</ul>
		</ul>
	</div>
</template>

<script>
	export default {
		methods:{
            toggleMenu: function(e){
            	$(e.srcElement).next().stop().slideToggle()
            	if($(e.srcElement).hasClass('down-jiantou')){
            		$(e.srcElement).removeClass('down-jiantou')
            		$(e.srcElement).addClass('right-jiantou')
            	}else{
            		$(e.srcElement).removeClass('right-jiantou')
            		$(e.srcElement).addClass('down-jiantou')
            	}
            }
        }
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sub-menu{
	height: 100%;
	display: flex;
	flex-direction: column;
}

.sub-menu .menu{
	flex: 1;
	overflow: auto;
}

.title{
	line-height: 70px;
	text-indent: 20px;
	background: #d5dae1;
	font-weight: bold;
}
.sub-menu ul li{
	line-height: 40px;
	cursor: pointer;
}
.sub-menu ul li:hover{
	background: #f3f5f7;
}
.sub-menu ul li span{
	display: inline-block;
	width: 30px;
	text-align: center;
}
.sub-menu ul li.right-jiantou span{
	display: inline-block;
	animation: right-jiantou 200ms ease 1 forwards;
	-moz-animation: right-jiantou 200ms ease 1 forwards;
	-webkit-animation: right-jiantou 200ms ease 1 forwards;
	-o-animation: right-jiantou 200ms ease 1 forwards;
}
.sub-menu ul li.down-jiantou span{
	display: inline-block;
	animation: down-jiantou 200ms ease 1 forwards;
	-moz-animation: down-jiantou 200ms ease 1 forwards;
	-webkit-animation: down-jiantou 200ms ease 1 forwards;
	-o-animation: down-jiantou 200ms ease 1 forwards;
}
.sub-menu ul ul li{
	padding-left: 38px;
}
.sub-menu ul ul li.active{
	background: #fff;
}

/*箭头向右*/
@keyframes right-jiantou{
	to {transform: rotate(-90deg);}
}
@-moz-keyframes right-jiantou{
	to {transform: rotate(-90deg);}
}
@-webkit-keyframes right-jiantou{
	to {transform: rotate(-90deg);}
}
@-o-keyframes right-jiantou{
	to {transform: rotate(-90deg);}
}
/*箭头向下*/
@keyframes down-jiantou{
	from {transform: rotate(-90deg);}
	to {transform: rotate(0deg);}
}
@-moz-keyframes down-jiantou{
	from {transform: rotate(-90deg);}
	to {transform: rotate(0deg);}
}
@-webkit-keyframes down-jiantou{
	from {transform: rotate(-90deg);}
	to {transform: rotate(0deg);}
}
@-o-keyframes down-jiantou{
	from {transform: rotate(-90deg);}
	to {transform: rotate(0deg);}
}
</style>