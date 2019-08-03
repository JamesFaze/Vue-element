<template lang="html">
    <div>
        <el-breadcrumb separator-class="el-icon-arrow-right" style="float:left; margin: 20px;">
            <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
            <el-breadcrumb-item>活动管理</el-breadcrumb-item>
        </el-breadcrumb>

        <div class="demo-input-suffix" style="float:left;margin:55px 0 20px -130px;">
            <el-input
                placeholder="请输入内容"
                prefix-icon="el-icon-search"
                v-model="input1">
            </el-input>
        </div>

        <el-button type="primary" icon="el-icon-search" style="margin: 55px 0 0 10px;">搜索</el-button>
        <el-button type="primary" icon="el-icon-d-caret" @click="handleButClick">高级搜索</el-button>
        <el-button type="primary" icon="el-icon-plus" style="float:right;margin: 55px 15px 0 0;">添加员工</el-button>
        <el-button type="success" icon="el-icon-bottom-right" style="float:right;margin: 55px 10px 0 0;">导出数据</el-button>
        <el-button type="success" icon="el-icon-top-left" style="float:right;margin: 55px 10px 0 0;">导入数据</el-button>

        <el-container style="height: 100%; border: 1px solid #eee;width:1670px; margin-left:20px;float:left;">
            <el-table
                :data="tableData"
                border
                style="width: 100%">

                <el-table-column
                fixed
                type="selection"
                width="35">
                </el-table-column>

                <el-table-column
                fixed
                prop="name"
                label="姓名"
                width="100">
                </el-table-column>

                <el-table-column
                prop="Job_number"
                label="工号"
                width="90">
                </el-table-column>

                <el-table-column
                prop="gender"
                label="性别"
                width="50">
                </el-table-column>

                <el-table-column
                prop="birthday"
                label="出生日期"
                width="100">
                </el-table-column>

                <el-table-column
                prop="ID_Card"
                label="身份证号码"
                width="180">
                </el-table-column>

                <el-table-column
                prop="marriage"
                label="婚姻状况"
                width="80">
                </el-table-column>

                <el-table-column
                prop="Nationality"
                label="民族"
                width="50">
                </el-table-column>

                <el-table-column
                prop="Birthplace"
                label="籍贯"
                width="80">
                </el-table-column>

                <el-table-column
                prop="political_status"
                label="政治面貌"
                width="80">
                </el-table-column>

                <el-table-column
                prop="e_mail"
                label="电子邮件"
                width="150">
                </el-table-column>
                
                <el-table-column
                prop="phone"
                label="电话号码"
                width="120">
                </el-table-column>

                <el-table-column
                prop="address"
                label="联系地址"
                width="200">
                </el-table-column>

                <el-table-column
                prop="Department"
                label="所属部门"
                width="80">
                </el-table-column>

                <el-table-column
                prop="position"
                label="职位"
                width="100">
                </el-table-column>

                <el-table-column
                prop="job_title"
                label="职称"
                width="100">
                </el-table-column>

                <el-table-column
                prop="Hire_form"
                label="聘用形式"
                width="80">
                </el-table-column>

                <el-table-column
                prop="Entry"
                label="入职日期"
                width="100">
                </el-table-column>

                <el-table-column
                prop="Turn_positive"
                label="转正日期"
                width="100">
                </el-table-column>

                <el-table-column
                prop="Contract_start"
                label="合同起始日期"
                width="110">
                </el-table-column>

                <el-table-column
                prop="Contract_ended"
                label="合同截至日期"
                width="110">
                </el-table-column>

                <el-table-column
                prop="Contract_period"
                label="合同期限"
                width="80">
                </el-table-column>

                <el-table-column
                prop="Education"
                label="学历"
                width="50">
                </el-table-column>

                <el-table-column
                fixed="right"
                label="操作"
                width="100">
                <template slot-scope="scope">
                    <el-button @click="handleClick(scope.row)" type="text" size="small">查看</el-button>
                    <el-button type="text" size="small">编辑</el-button>
                </template>
                </el-table-column>
            </el-table>
        </el-container>

        <el-button type="danger" disabled style="float:left; margin-top:10px; margin-left:20px">危险按钮</el-button>
        <el-pagination
            background
            layout="prev, pager, next"
            :total="1000"
            style="float: right; margin-top:10px;margin-right:5px">
        </el-pagination>
    </div>
</template>

<script>
export default {
    name: 'ReCount',
    methods: {
      handleClick(row) {
        console.log(row);
      },
      handleButClick:function () {
          alert("aaaa")
      }
    },
    data() {
      return {
        input1: '',
        tableData: [{
          name: '江南一点雨',
          Job_number: '00000010',
          gender: '男',
          birthday: '1990-01-01',
          ID_Card: "610122199001011256",
          marriage: '未婚',
          Nationality: '汉族',
          Birthplace: '陕西西安',
          political_status: '中共党员',
          e_mail: 'laowang@qq.com',
          phone: '18565558897',
          address: '广东省广州市天河区冼村路',
          Department: '市场部',
          position: '研发工程师',
          job_title: '高级工程师',
          Hire_form: '劳务合同',
          Entry: '2018-01-01',
          Turn_positive: '2018-04-01',
          Contract_start: '2018-01-01',
          Contract_ended: '2020-01-01',
          Contract_period: '2年',
          Education: '本科'
        }]
      }
    }
  }
</script>

<style scoped>
</style>