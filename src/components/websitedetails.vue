<template>
  <div>
    <el-container>
      <el-header class="el-header" style="height: 200px">Header</el-header>
      <el-container>
        <el-aside width="400px" style="height: 900px">Aside</el-aside>
        <el-main class="el-main" style="height: 900px">Main</el-main>
      </el-container>

      <el-footer class="el-footer" style="height: 200px">Footer</el-footer>
    </el-container>
  </div>
</template>

<script>
export default {};
</script>

<style>
.el-header {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  /* line-height: 300px; */
}
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  /* line-height: 200px; */
  /* footer的高度不能在这设置，header同理 */
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  /* line-height: 600px; */
}
</style>