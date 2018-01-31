<template>
  <div id="app">
    <img src="./assets/logo.png">
    <ul>
      <li @click="showMessage">message全局提示</li>
      <li @click="showModal">modal对话框</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  methods: {
    showModal () {
      this.$Modal({
        type: 1, // 标题；可选，默认1有标题；0无标题
        cancel: null, // 点击取消回调函数；可选，默认无
        sure: null, // 点击确定回调函数；可选，默认无
        btn: ['取消', '确定'], // 按钮；可选，默认'取消','确定'两个按钮
        btnShow: true, // 取消按钮是否隐藏；可选，默认显示；配合按钮使用
        title: '系统提示', // 标题；可选，默认显示
        content: '<p>这是一个modal对话框</p>' // 提示内容；可选，html模板
      })
    },
    showMessage () {
      this.$Message({
        type: 'info', // 提示，可选，默认info提示；error失败；success成功
        content: '没有提示内容' // 可选，默认提示
      })
    }
  }
}
</script>

<style>
html {
  font-size: 20px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
li {
  padding: 10px;
}
</style>
