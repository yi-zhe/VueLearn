<template>
  <h1 v-text="msg" ref="title"></h1>
  <button ref="btn" @click="showDOM">点我输出上方的DOM元素</button>
  <School ref="sch" />
</template>

<script>
import School from './components/School.vue'

export default {
  name: 'App',
  components: {
    School
  },
  data() {
    return {
      msg: '欢迎学习'
    }
  },
  methods: {
    showDOM() {
      console.log(this.$refs.title) // 真实DOM
      console.log(this.$refs.btn)   // 真实DOM
      console.log(this.$refs.sch)   // ViewComponent实例的代理对象
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
