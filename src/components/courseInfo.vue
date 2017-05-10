<template>
    <div class="course-info">
      <div class="info-item">
        <span>用户提供PPT:</span>
        <a class="btn" href="javascript:void(0)" v-if="upLoad.PPT">点击预览</a>
        <a class="btn" href="javascript:void(0)" v-else>点击上传</a>
      </div>
      <div class="info-item">
        <span>用户提供的脚本：</span>
        <a class="btn" href="javascript:void(0)" v-if="upLoad.script">点击预览</a>
        <a class="btn" href="javascript:void(0)" v-else>点击上传</a>        
      </div>
      <div class="info-item">
        <span>用户提供的其他资料：</span>
        <a class="btn" href="javascript:void(0)" v-if="upLoad.others">点击预览</a>
        <a class="btn" href="javascript:void(0)" v-else>点击上传</a>        
      </div>
    </div>
</template>

<script>

export default {
    data(){
      return{
        upLoad:{
          PPT:true,
          script:false,
          others:false
        }
      }
    }


  // 暂时没有模拟数据，需要获得文件上传状态和 hash值
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
  .info-item{
    flex: 1;
  }
  .btn{
    display: block;
    text-decoration: none;
    padding: 5px 15px;
    box-shadow: 2px 2px 5px;
    cursor: pointer;
  }
</style>
