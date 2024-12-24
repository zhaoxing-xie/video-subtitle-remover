<template>
  <div class="container">
    <h1>AI恋爱婚姻契合度测试</h1>
    <test-form></test-form>
  </div>
</template>

<script>
import TestForm from './components/TestForm.vue'

export default {
  name: 'App',
  components: {
    TestForm  // 注册TestForm组件
  }
}
</script>

<style>
.container {
  text-align: center;
  margin-top: 60px;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
  padding: 30px;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  background-color: #fff2f4;
  border: 1px solid #ebeef5;
}

h1 {
  color: #409EFF;
  margin-bottom: 20px;
  font-size: 24px;
}

/* 添加全局样式 */
body {
  margin: 0;
  padding: 0;
  background-color: #f5f7fa;
}

/* 移动端适配 */
@media screen and (max-width: 768px) {
  .container {
    margin-top: 30px;
  }
  
  h1 {
    font-size: 20px;
    padding: 0 15px;
  }
}

.el-button {
    width: 200px;
    margin-top: 20px;
    transition: all 0.3s;
}

.el-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 2px 12px rgba(64, 158, 255, 0.4);
}
</style>