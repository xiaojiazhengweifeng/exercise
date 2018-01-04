<template>
    <el-table
      :data="tableData5"
      style="width: 100%"
      size="mini">
      <el-table-column type="expand">
        <template slot-scope="props">
          <el-form label-position="left" inline class="demo-table-expand">
            <el-form-item label="商品名称">
              <span>{{ props.row.name }}</span>
            </el-form-item>
            <el-form-item label="所属店铺">
              <span>{{ props.row.shop }}</span>
            </el-form-item>
            <el-form-item label="商品 ID">
              <span>{{ props.row.id }}</span>
            </el-form-item>
            <el-form-item label="店铺 ID">
              <span>{{ props.row.shopId }}</span>
            </el-form-item>
            <el-form-item label="商品分类">
              <span>{{ props.row.category }}</span>
            </el-form-item>
            <el-form-item label="店铺地址">
              <span>{{ props.row.address }}</span>
            </el-form-item>
            <el-form-item label="商品描述">
              <span>{{ props.row.desc }}</span>
            </el-form-item>
          </el-form>
        </template>
      </el-table-column>
      <el-table-column
        label="姓名"
        prop="name">
      </el-table-column>
      <el-table-column
        label="手机号"
        prop="phone">
      </el-table-column>
      <el-table-column
        label="员工状态"
        prop="status"
        :formatter="getStatusText">
      </el-table-column>
      <el-table-column
        label="部门"
        prop="team">
      </el-table-column>
      <el-table-column
        label="操作">
        <template slot-scope="scope">
          <el-button
            type="text"
            size="small">
            开除
          </el-button>
          <el-button
            type="text"
            size="small">
            离职
          </el-button>
          <el-button
            type="text"
            size="small">
            修改密码
          </el-button>
        </template>
      </el-table-column>
    </el-table>
</template>

<script>
export default {
  props: {
    tableData5: {
      default: []
    }
  },
  data () {
    return {
      msg: 'tab'
    }
  },
  methods: {
    getStatusText (...rest) {
      let statusText = ['在职', '离职', '开除']
      return statusText[rest[2]]
    }
  }
}
</script>

<style scoped lang="less">
</style>
