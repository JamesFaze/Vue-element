<template>
    <div>
      <el-container style="float:left;height: 893px; border: 1px solid #eee;width:200px;">
        <el-aside width="200px" style="background-color: rgb(236, 236, 236)">
          <el-menu :default-openeds="['1', '3']">
            <el-submenu index="2">
              <template slot="title"><i class="el-icon-user scolor"></i>员工资料</template>
              <el-menu-item-group>
                <el-menu-item index="1-1">基本资料</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="4">
              <template slot="title"><i class="el-icon-postcard scolor"></i>人事管理</template>
              <el-menu-item-group>
                <el-menu-item index="2-1">员工奖罚</el-menu-item>
                <el-menu-item index="2-2">员工培训</el-menu-item>
                <el-menu-item index="2-3">员工调薪</el-menu-item>
                <el-menu-item index="2-4">员工调动</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="6">
              <template slot="title"><i class="el-icon-money scolor"></i>薪资管理</template>
              <el-menu-item-group>
                <el-menu-item index="3-1">工资帐套管理</el-menu-item>
                <el-menu-item index="3-2">员工帐套管理</el-menu-item>
                <el-menu-item index="3-3">工资表管理</el-menu-item>
                <el-menu-item index="3-4">月末处理</el-menu-item>
                <el-menu-item index="3-5">工资表查询</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="8">
              <template slot="title"><i class="el-icon-data-analysis scolor"></i>统计管理</template>
              <el-menu-item-group>
                <el-menu-item index="3-1">综合信息统计</el-menu-item>
                <el-menu-item index="3-2">员工积分统计</el-menu-item>
                <el-menu-item index="3-3">人事信息统计</el-menu-item>
                <el-menu-item index="3-4">人事记录统计</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-submenu index="10">
              <template slot="title"><i class="el-icon-setting scolor"></i>系统管理</template>
              <el-menu-item-group>
                <el-menu-item index="3-1">基础信息设置</el-menu-item>
                <el-menu-item index="3-2">系统管理</el-menu-item>
                <el-menu-item index="3-3">操作日志管理</el-menu-item>
                <el-menu-item index="3-4">操作员管理</el-menu-item>
                <el-menu-item index="3-5">备份恢复数据库</el-menu-item>
                <el-menu-item index="3-6">初始化数据</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
          </el-menu>
        </el-aside>
      </el-container>
    </div>
</template>

<script>
export default {
  name: 'ReNav',
}
</script>

<style scoped>
.el-header {
  background-color: #B3C0D1;
  color: #333;
  line-height: 60px;
  }
.el-aside {
  color: #333;
  }
.weirs{
  float: left;
  font-size: 20px;
  color:#fff;
}
.bgcolor{
  background: #20a0ff;
}
.scolor{
  color: #20a0ff;
}
</style>
