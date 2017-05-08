<template>
  <div>
		<!--每个模块的标题指定类由父组件控制样式‘lesson-item-title’-->
		<div class="lesson-item-title">
			<p>began-time</p><p>end-time</p>
		</div>
		<span>时间进度：</span>
		<div class="time-progress">
			<div class="time-process"></div>
		</div>
		<div class="course">
			<div class="course-item">策划脚本</div>
			<div class="course-item">PPT文件</div>
			<div class="course-item">脚本意见</div>
			<div class="course-item">拍摄源视频</div>
			<div class="course-item">视频模板</div>
			<div class="course-item">模板意见</div>
			<div class="course-item">定稿视频</div>
			<div class="course-item">视频意见</div>
		</div>
	</div>
</template>

<script>
export default {

}
</script>

<style>
	.lesson-item-title p{
		float:left;
	}
	.course{
		display:flex;
	}
	.course-item{
		flex:1;
	}
</style>
