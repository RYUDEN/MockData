<template>
    <div class="course-info">
      <div class="info-item">
        <span>用户提供PPT:</span>
      </div>
      <div class="info-item">
        <span>用户提供的脚本：</span>
      </div>
      <div class="info-item">
        <span>用户提供的其他资料：</span>
      </div>
    </div>
</template>

<script>

export default {
//    computed:{
//        lessons(){
//            return this.$store.state.data.lessons
//        }
//    }
}
</script>

<style scoped>
  .course-info{
    display: flex;
  }
  info-item{
    flex: 1;
  }
</style>
