<template>
  <div id="app">
    <courseBase></courseBase>
    <lessonNum></lessonNum>
    <lessonName></lessonName>
    <lessonMain></lessonMain>
    <courseInfo></courseInfo>
    <lessonMember></lessonMember>
    <lessonLog></lessonLog>
    <lessonOperation></lessonOperation>
  </div>
</template>

<script>
import courseBase from './components/courseBase'
import courseInfo from './components/courseInfo'
import lessonLog from './components/lessonLog'
import lessonMain from './components/lessonMain'
import lessonMember from './components/lessonMember'
import lessonName from './components/lessonName'
import lessonNum from './components/lessonNum'
import lessonOperation from './components/lessonOperation'
import Vue from 'vue'
import Vuex from 'vuex'
Vue.use(Vuex);
const store = new Vuex.Store({
    state: {
      data: null//保存当前章节的信息
    },
    mutations: {
			data(state, payload){
				state.data=payload
			}
		}
})
console.log(this.store)

export default {
  name: 'app',
  components: {
    courseBase,
    lessonMain,
    lessonLog,
    lessonMember,
    lessonName,
    lessonNum,
    lessonOperation,
    courseInfo
  },
  created(){
    this.$http.get('https://www.easy-mock.com/mock/591009d6f926ef14e26a56e8/lithii/main').then(response => {
        var res = response.body;
        
    })
  }
}

</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
