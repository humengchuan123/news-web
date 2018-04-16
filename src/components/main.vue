<template>
  <div>
	 <div class="header">
		<ul class="header-content">
			<li class="header-item">推荐</li>
			<li class="header-item">新闻</li>
			<li class="header-item">娱乐</li>
			<li class="header-item">体育</li>
			<li class="header-item">图片</li>
			<li class="header-item">科技</li>
		</ul>
	</div>
	<div class="banner-content">
		  	 <v-banner></v-banner>
	</div>
  </div>
	
</template>

<script>
import banner from '../components/banner'
export default{
	components: {
		"v-banner" : banner
	},
	data () {
		return {}
	}
}	
</script>

<style lang="scss" scoped>
@function px2rem($px) {
	$rem: 37.5px;
	@return ($px / $rem) + rem;
}
.header {
	height: px2rem(80px);
	width: 100%;
	background-color: red;
	padding-left: px2rem(80px);
	.header-item {
		font-size: px2rem(36px);
		color: #ffcdce;
		float: left;

		margin-right: px2rem(20px);
		line-height: px2rem(80px);

		&:nth-child(2) {
			color: #fff;
			font-size: px2rem(40px);
		}
	}
}
.header-content li {
	margin: 0 px2rem(20px);
}
.banner-content{
	display: block;
	width: 100%;
	height: px2rem(400px);
	background-color: #eee;
}
</style>