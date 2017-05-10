<template>
  <div>
      <p>责任人：</p>
      <div>
        <p>脚本策划：</p>
        <select name="脚本策划">
          <option v-for="manager in managers">
          {{ manager}}
          </option>
        </select>
      </div>
      <div>
        <p>PPT制作：</p>
        <select name="PPT制作" >
          <option v-for="manager in managers">
          {{ manager}}
          </option>
        </select>
      </div>
      <div>
        <p>拍摄人员：</p>
        <select name="拍摄人员">
          <option v-for="manager in managers">
          {{ manager}}
          </option>
        </select>
      </div>
      <div>
        <p>后期人员：</p>
        <select name="后期人员">
          <option v-for="manager in managers">
          {{ manager}}
          </option>
        </select>
      </div>
  </div>
</template>

<script>
export default {
  computed:{
    managers(){
      return this.$store.state.data.project.personnel
    }
  }
}
</script>

<style>

</style>
