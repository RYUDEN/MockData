<template>
  <div id="log">
      <p>最新日志：</p>
      <p v-for="log in lesssons.log" v-if="$index<5">
          {{log.log}}
      </p>
      <a v-if="lessons.log.length>5">更多</a>
  </div>
</template>

<script>
export default {
    computed:{
      
    }
}
</script>

<style>

</style>
