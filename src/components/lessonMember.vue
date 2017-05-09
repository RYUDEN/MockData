<template>
  <div id="">
      <p>责任人：</p>
      <div>
        <p>脚本策划：</p>
        <select name="脚本策划" id="">
          <option v-for="manager in lessons.managers">
          {{ manager.managers}}
          </option>
        </select>
      </div>
      <div>
        <p>PPT制作：</p>
        <select name="PPT制作" id="">
          <option v-for="manager in lessons.managers">
          {{ manager.managers}}
          </option>
        </select>
      </div>
      <div>
        <p>拍摄人员：</p>
        <select name="拍摄人员" id="">
          <option v-for="manager in lessons.managers">
          {{ manager.managers}}
          </option>
        </select>
      </div>
      <div>
        <p>后期人员：</p>
        <select name="后期人员" id="">
          <option v-for="manager in lessons.managers">
          {{ manager.managers}}
          </option>
        </select>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
