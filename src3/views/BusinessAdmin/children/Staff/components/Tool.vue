<template>
    <el-row>
      <el-col :span="12">
        <el-form :inline="true"  class="demo-form-inline">
          <el-form-item >
            <el-input placeholder="搜索姓名，手机号" size="mini" prefix-icon="el-icon-search"></el-input>
          </el-form-item>
          <el-form-item>
            <el-button type="primary" size="mini">查询</el-button>
          </el-form-item>
        </el-form>
      </el-col>
      <el-col :span="12">
        <el-form :inline="true"  class="demo-form-inline">
          <el-form-item >
            <el-button type="primary" size="mini">添加员工</el-button>
          </el-form-item >
        </el-form>
      </el-col>
    </el-row>
</template>

<script>
export default {
  data () {
    return {
      msg: 'tab'
    }
  }
}
</script>

<style scoped lang="less">
</style>
