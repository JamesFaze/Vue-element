<template>
    <div class="main">
      <div class="div1">
        <p>系统登陆</p>
        <el-form :model="ruleForm" status-icon :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
          <el-form-item label="" prop="text" style="margin-left: -95px;">
            <el-input type="text" v-model="ruleForm.text" autocomplete="off"></el-input>
          </el-form-item>
          <el-form-item label="" prop="pass" style="margin-left: -95px;">
            <el-input type="password" v-model="ruleForm.pass" autocomplete="off"></el-input>
          </el-form-item>
          <el-checkbox v-model="checked" class="div2">记住密码</el-checkbox>
          <el-form-item>
            <el-button type="primary" @click="submitForm('ruleForm')" style="width:345px;margin-left:-95px;">提交</el-button>
          </el-form-item>
      </el-form>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HomeLogin',
  data () {
    var validateText = (rule, value, callback) => {
      if (value === '') {
        callback(new Error('请输入账号'))
      } else {
        if (this.ruleForm.text !== '') {
          this.$refs.ruleForm.validateField('text')
        }
        callback()
      }
    }
    var validatePass = (rule, value, callback) => {
      if (value === '') {
        callback(new Error('请输入密码'))
      } else {
        if (this.ruleForm.pass !== '') {
          this.$refs.ruleForm.validateField('pass')
        }
        callback()
      }
    }
    // var validatePass2 = (rule, value, callback) => {
    //   if (value === '') {
    //     callback(new Error('请再次输入密码'))
    //   } else if (value !== this.ruleForm.pass) {
    //     callback(new Error('两次输入密码不一致!'))
    //   } else {
    //     callback()
    //   }
    // }
    return {
      checked: true,
      ruleForm: {
        text: '',
        pass: ''
      },
      rules: {
        text: [
          { validator: validateText, trigger: 'blur' }
        ],
        pass: [
          { validator: validatePass, trigger: 'blur' }
        ]
      }
    }
  },
  methods: {
    submitForm (formName) {
      this.$refs[formName].validate((valid) => {
        if (valid) {
          alert('submit!')
        } else {
          console.log('error submit!!')
          return false
        }
      })
    },
    resetForm (formName) {
      this.$refs[formName].resetFields()
    }
  }
}
</script>

<style scoped>
  .main{
    width: 100%;
    height: 100%;
    margin: 0 auto;
    padding: 0;
  }
  .div1{
    border-radius: 15px;
    background-clip: padding-box;
    margin: 180px auto;
    width: 350px;
    padding: 35px 35px 15px;
    background: #fff;
    border: 1px solid #eaeaea;
    box-shadow: 0 0 25px #cac6c6;
  }
  .div1 p{
    font-size: 18px;
    text-align: center;
    padding-bottom: 10px;
    font-weight: bold
  }
  .div2{
    margin-left: 130px;
    margin-bottom: 25px;
  }
</style>
