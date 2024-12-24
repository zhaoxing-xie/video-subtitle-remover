<template>
  <div class="test-form">
    <el-form :model="form" label-width="120px">
      <el-form-item label="您的姓名">
        <el-input v-model="form.name1" placeholder="请输入您的姓名"></el-input>
      </el-form-item>
      
      <el-form-item label="对方姓名">
        <el-input v-model="form.name2" placeholder="请输入对方姓名"></el-input>
      </el-form-item>
      
      <el-form-item label="您的生日">
        <el-date-picker v-model="form.birth1" type="date" placeholder="选择日期"></el-date-picker>
      </el-form-item>
      
      <el-form-item label="对方生日">
        <el-date-picker v-model="form.birth2" type="date" placeholder="选择日期"></el-date-picker>
      </el-form-item>
      
      <el-form-item>
        <el-button type="primary" @click="onSubmit">开始测试</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'TestForm',
  data() {
    return {
      form: {
        name1: '',
        name2: '',
        birth1: '',
        birth2: ''
      }
    }
  },
  methods: {
    onSubmit() {
      // 表单验证
      if (!this.form.name1 || !this.form.name2) {
        alert('请输入双方姓名')
        return
      }
      if (!this.form.birth1 || !this.form.birth2) {
        alert('请选择双方生日')
        return
      }
      
      // 格式化日期
      const formatDate = (date) => {
        if (!date) return ''
        const d = new Date(date)
        return `${d.getFullYear()}年${d.getMonth() + 1}月${d.getDate()}日`
      }

      // 计算结果（示例）
      const result = {
        names: `${this.form.name1} 和 ${this.form.name2}`,
        birthDays: `${formatDate(this.form.birth1)} - ${formatDate(this.form.birth2)}`
      }
      
      // 显示结果
      alert(`测试完成！\n\n姓名：${result.names}\n生日：${result.birthDays}\n\n契合度：88%\n（测试数据仅供参考）`)
      
      // 输出到控制台
    
    }
  }
}
</script>

<style>
.test-form {
  max-width: 500px;
  margin: 0 auto;
  padding: 30px;
  background-color: #f8f9fa;
  border-radius: 8px;
}

.el-form-item {
  margin-bottom: 25px;
}

.el-date-picker {
  width: 100%;
}

/* 添加输入框hover效果 */
.el-input:hover {
  box-shadow: 0 0 8px rgba(64, 158, 255, 0.2);
}

@media screen and (max-width: 768px) {
  .test-form {
    padding: 10px;
  }
  
  .el-form-item__label {
    float: none;
    text-align: left;
    line-height: 32px;
  }
}

.el-button {
    width: 100%;
    margin-top: 30px;
    transition: all 0.3s;
    height: 40px;
    font-size: 16px;
}

.el-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 2px 12px rgba(64, 158, 255, 0.4);
}
</style>
