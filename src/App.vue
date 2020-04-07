<template>
  <div id="app">
    <alert type="success" title="这是一段成功提示的信息" @defclick='clickHandle' />
    <alert @defclick="clickHandle" />
    <alert type="warning" title="这是一段警告提示的信息" @defclick='clickHandle' />
    <alert type="error" title="这是一段错误提示的信息" @defclick='clickHandle' />
  </div>
</template>

<script>
import alert from '@/components/alert'

export default {
  name: 'App',
  components: {
    alert
  },
  methods: {
    clickHandle() {
      console.log('test')
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
