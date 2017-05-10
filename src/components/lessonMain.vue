<template>
  <div>
		<!--每个模块的标题指定类由父组件控制样式‘lesson-item-title’-->
		<div class="lesson-item-title">
			<p>开始时间 {{main.start}} </p><p>结束时间{{main.end}}</p>
		</div>
		<span>时间进度：</span>
		<div class="time-progress">
			<div class="time-process"></div>
		</div>
		<div class="course">
			<div class="course-item">策划脚本
        <p>{{main.planningScript.length}}</p>
      </div>
			<div class="course-item">PPT文件
        <p>{{main.pptFile.length}}</p>
      </div>
			<div class="course-item">脚本意见
      </div>
			<div class="course-item">拍摄源视频
        <p>{{main.sourceVideo.length}}</p>
      </div>
			<div class="course-item">视频模板
        <p>{{main.videoModel.length}}</p>
      </div>
			<div class="course-item">模板意见</div>
			<div class="course-item">定稿视频
        <p>{{main.finalVideo.length}}</p>
      </div>
			<div class="course-item">视频意见</div>
		</div>
	</div>
</template>

<script>
export default {
  props:{
      main:{

    }
  }
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
