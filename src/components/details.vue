<template>
  <div>
    <el-container>
      <el-header class="el-header" style="height: 150px">
        <div class="signin">
          <div class="signinbutton">sign in</div>
          <div class="signinbutton1">sign up</div>
        </div>
        <img class="img1" src="../assets/logo.png" height="100px" />
      </el-header>
      <div class="position"></div>
      <div class="detailsearch">
        <div class="searchlogo">
          <img src="../assets/weblogo.png" />
        </div>

        <el-autocomplete
          class="inline-input"
          :fetch-suggestions="querySearch"
          placeholder="Please enter the keyword you want to search"
          :trigger-on-focus="false"
          @select="handleSelect"
          @keyup.enter.native="search"
        ></el-autocomplete>
        <el-button type="primary" icon="el-icon-search" @click="search"
          >Search</el-button
        >
      </div>
      <el-main class="el-main">
        <div class="list">
          <div
            class="item"
            v-for="item in [1, 2, 3, 4, 5, 6, 7, 8, 9]"
            :key="item.id"
          >
            <el-row>
              <el-col :span="24">
                <div class="information-title">
                  一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；
                </div>
              </el-col>
            </el-row>
            <el-row>
              <el-col :span="24">
                <div class="information-writer">
                  一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；
                  一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；
                  一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；
                </div>
              </el-col>
            </el-row>
            <el-row>
              <el-col :span="24">
                <div class="information-summary">
                  一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；
                  一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；
                  一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；一行文字过多时，隐藏省略显示；
                </div>
              </el-col>
            </el-row>
          </div>
        </div>
      </el-main>
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
        <div class="banquan">&copy;版权所有BJTU</div></el-footer
      >
    </el-container>
  </div>
</template>
<script>
export default {
  name: "details",
};
</script>

<style scoped>
.el-header {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  /* line-height: 300px; */
  background: url(../assets/sky2.jpg);
  background-image: url(../assets/sky2.jpg);
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
  color: #333;
  text-align: center;
  /* line-height: 600px; */
  padding: 20px 150px 20px 150px;
  background-color: #fff;
}

.list {
  padding: 40px;
}
.item {
  margin-bottom: 20px;
}
.img1 {
  margin-top: 50px;
}

.information-title {
  font-size: 18px;
  width: 100%; /*一定要设置宽度，或者元素内含的百分比*/
  overflow: hidden; /*溢出的部分隐藏*/
  white-space: nowrap; /*文本不换行*/
  text-overflow: ellipsis; /*ellipsis:文本溢出显示省略号（...）；clip：不显示省略标记（...），而是简单的裁切*/
  text-align: left;
  color: #0071bc;
}
.information-writer {
  font-size: 16px;
  width: 100%; /*一定要设置宽度，或者元素内含的百分比*/
  overflow: hidden; /*溢出的部分隐藏*/
  white-space: nowrap; /*文本不换行*/
  text-overflow: ellipsis; /*ellipsis:文本溢出显示省略号（...）；clip：不显示省略标记（...），而是简单的裁切*/
  text-align: left;
  color: #212121;
}
.information-summary {
  font-size: 16px;
  width: 100%; /*一定要设置宽度，或者元素内含的百分比*/
  overflow: hidden; /*溢出的部分隐藏*/
  white-space: nowrap; /*文本不换行*/
  text-overflow: ellipsis; /*ellipsis:文本溢出显示省略号（...）；clip：不显示省略标记（...），而是简单的裁切*/
  text-align: left;
  color: #4d8055;
}
.inline-input {
  width: 50%;
}

/deep/.el-button {
  background-color: #102785;
  border-color: #102785;
}
.detailsearch {
  height: 70px;

  background-color: #f1f1f1;
}
.position {
  height: 20px;
  background-color: #f1f1f1;
}
.searchlogo {
  float: left;
  padding-left: 12%;
  padding-right: 5%;
}
.signinbutton {
  margin-top: 10px;
  margin-right: -10px;
  float: right;
  padding: 10px 10px;
  color: #f9fafc;
  font-size: 20px;
  border: 1px solid rgba(255, 255, 255, 0.5);
}
.signinbutton1 {
  margin-top: 10px;
  margin-right: 10px;
  float: right;
  padding: 10px 10px;
  color: #f9fafc;
  font-size: 20px;
  border: 1px solid rgba(255, 255, 255, 0.5);
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