<template>
  <div class="page-content">
    <Tool/>
    <TableBox :tableData5="tableData5"/>
  </div>
</template>

<script>
import Tool from './components/Tool'
import TableBox from './components/TableBox'

export default {
  name: 'Home',
  data () {
    return {
      tableData5: []
    }
  },
  components: {
    TableBox,
    Tool
  },

  created () {
    this.$http.get('api/getStaffList').then((data) => {
      console.log(data)
      this.tableData5 = data.data
    })
  }
}
</script>

<style scoped lang="less">
.page-content{
  width: 100%;
}
.demo-table-expand {
  font-size: 0;
}
.demo-table-expand label {
  width: 90px;
  color: #99a9bf;
}
.demo-table-expand .el-form-item {
  margin-right: 0;
  margin-bottom: 0;
  width: 50%;
}
</style>
