<template>
  <div id="log">
      <p>最新日志：</p>
       <p v-for="(log,index) in logs" v-if="index<5">
           {{log}}
       </p>
       <a class="toggle-button" href="javascript:void(0)" v-if="this.logs.length>=5" @click="toggle()">更多</a>
       <div v-if="panelOn">
         <p v-for="log in logs">{{log}}</p>
       </div>
  </div>
</template>

<script>
export default {
    data(){
      return{
          panelOn:false
      }
    },
    props:{
        logs:{
        }
    },
    methods:{
        toggle(){
            return this.panelOn = !this.panelOn ,
            console.log(panelOn)
        }
    }
}
</script>

<style scoped>
  .toggle-button{

  }
</style>
