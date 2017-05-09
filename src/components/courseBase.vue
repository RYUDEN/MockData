<template>
  <div id="courseBase">
     <p>项目名称：{{project.name}}</p>
		<p>学校：{{project.school}}</p>
		<p>学院：{{project.school}}</p>
		<p>项目牵头人：{{project.guideTeacher}}</p>
		<p>项目经理：{{project.anthor}}</p>
		<p v-for="person in personnel">项目参与人员：{{peosonnel.person}}</p>
		<hr>
		<p>创建人：{{project.anthor}}</p>
		<p>创建时间：{{project.create}}</p>
		<p>课程名称：{{project.name}}</p>
		<p>课程负责人：{{project.manager.lessonManager}}</p>
		<p>后期负责人：{{project.manager.postManager}}</p>
		<p>运维负责人：{{project.manager.operationManager}}</p>
  </div>
</template>

<script>
export default {
  name: 'courseBase',
 
}
</script>

<style>

</style>
