<template lang="html">
    <div>
        <el-container>
            <el-header style="text-align: right; font-size: 12px" class="bgcolor">
            <el-dropdown>
                <i class="el-icon-bell" style="margin-right: 15px"></i>
                <el-dropdown-menu slot="dropdown">
                <el-dropdown-item>查看</el-dropdown-item>
                <el-dropdown-item>新增</el-dropdown-item>
                <el-dropdown-item>删除</el-dropdown-item>
                </el-dropdown-menu>
            </el-dropdown>
            <span class="weirs">微人事</span>
            <span>系统管理员</span>
            <div style="float: right; margin-left: 10px; margin-top: 10px;">
                    <el-avatar icon="el-icon-user-solid"></el-avatar>
                </div>
            </el-header>
      </el-container>
    </div>
</template>

<script>
export default {
    name: 'ReTopnav'
}
</script>

<style scoped>
.el-header {
  background-color: #B3C0D1;
  color: #333;
  line-height: 60px;
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
