<template>
  <div>
    <el-container>
      <el-header class="el-header" style="height: 200px">Header</el-header>
      <el-container>
        <el-aside width="600px" style="height: 1100px">Aside</el-aside>
        <el-main class="el-main" style="height: 1100px">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>introduction</span>
            </div>
            <span>这里是网站的简介</span>
          </el-card>
          <div class="white"></div>
          <el-card>
            <div slot="header" class="clearfix">
              <span>主要文献</span>
            </div>
            <div v-for="o in 10" :key="o" class="text item">
              {{ "列表内容 " + o }}
            </div>
          </el-card>
        </el-main>
      </el-container>

      <el-footer class="el-footer" style="height: 200px">
        <div class="footer"></div>
        <el-row :gutter="20">
          <el-col :span="6"
            ><div class="grid-content bg-purple">
              <a href="#" class="footerwriter">Contact us</a>
            </div></el-col
          >
          <el-col :span="6"
            ><div class="grid-content bg-purple">
              <a href="#" class="footerwriter">help</a>
            </div></el-col
          >
          <el-col :span="6"
            ><div class="grid-content bg-purple">
              <a href="#" class="footerwriter">help</a>
            </div></el-col
          >
          <el-col :span="6"
            ><div class="grid-content bg-purple">
              <a href="#" class="footerwriter">Accessibility</a>
            </div></el-col
          >
        </el-row>
        <el-row :gutter="20">
          <el-col :span="6"
            ><div class="picture">
              <a href="#" class="footerwriter"
                ><i class="el-icon-phone-outline"></i
              ></a>
              <a href="#" class="footerwriter"
                ><i class="el-icon-chat-dot-round"></i
              ></a>
              <a href="#" class="footerwriter"
                ><i class="el-icon-share"></i
              ></a></div
          ></el-col>
          <el-col :span="6"
            ><div class="grid-content bg-purple">
              <a href="#" class="footerwriter">help</a>
            </div></el-col
          >
          <el-col :span="6"
            ><div class="grid-content bg-purple">
              <a href="#" class="footerwriter">Careers</a>
            </div></el-col
          >
          <el-col :span="6"
            ><div class="grid-content bg-purple">
              <a href="#" class="footerwriter">Help</a>
            </div></el-col
          >
        </el-row>
        <el-divider><a href="#" class="fenge">mpaper.com</a></el-divider>
        <div class="banquan">&copy;版权所有BJTU</div>
      </el-footer>
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
  background: url(../assets/background.jpg);
  background-image: url(../assets/background.jpg);
  background-position-x: center;
  background-position-y: center;
  background-size: cover;
  background-attachment: initial;
  background-origin: initial;
  background-clip: initial;
}
.el-footer {
  background-color: #062b5a;
  color: #fff;
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

.clearfix {
  font-size: 20px;
}
.item {
  margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}
.white {
  padding: 40px;
}

.bg-purple-dark {
  background: #99a9bf;
}

.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;

  font-size: 19px;
}
.footer {
  padding: 15px;
}
.footerwriter {
  color: #fff;
  text-decoration: none;
}
.fenge {
  text-decoration: none;
}
.banquan {
  text-align: center;
}
.picture {
  border-radius: 4px;
  font-size: 30px;
}
</style>