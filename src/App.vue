<template>
  <div id="app">
    <courseBase></courseBase>
    <lessonMain></lessonMain>
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
      data: null,//保存当前章节的信息
      course:null,//保存所有课程的信息
      status: null
    },
});

export default {
  name: 'app',
  components: {
    courseBase,
    lessonMain
  },
  created(){
    this.$http.get('https://www.easy-mock.com/mock/591009d6f926ef14e26a56e8/lithii/main').then(response => {
        this.someData = response.body;
    }
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
