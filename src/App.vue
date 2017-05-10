<template>
  <div id="app">
    <div class="project-preview">
      <course-base></course-base>
      <course-info></course-info>
    </div>
    <div class="lesson-list" v-for="(lesson,key) in this.$store.state.data.lessons">
      <div class="item-list item">
        <lesson-num :num="key"></lesson-num>
      </div>
      <div class="item-name item">
        <lesson-name :name="lesson"></lesson-name>
      </div>
      <div class="item-main item">
        <lesson-main :main="lesson"></lesson-main>
      </div>
      <div class="item-member item">
        <lesson-member></lesson-member>
      </div>
      <div class="item-log item">
        <lesson-log :logs="lesson.log"></lesson-log>
      </div>
      <div class="item-operation item">
        <lesson-operation :operation="lesson"></lesson-operation>
      </div>
    </div>
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
      data:'',//保存当前章节的信息
    },
    mutations: {
			data(state, payload){
				state.data=payload
			}
		}
})

export default {
  store,
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
        this.$store.commit('data',res)
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
}
  .lesson-item-title{

  }
  .lesson-list{
    position: relative;
    display: block;
    width: 100%;
  }
  .item{
    display: block;
    flex:1;
  }
</style>
