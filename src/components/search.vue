<template>
  <div>
    <el-container>
      <el-header class="el-header" style="height: 300px">
        <div class="signin">
          <div class="signinbutton">sign in</div>
          <div class="signinbutton1">sign up</div>
        </div>
        <img src="../assets/logo.png" height="100px" />
        <!-- 水平的导航栏菜单，有六个分类 -->
        <el-menu
          :default-active="activeIndex2"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#fff"
          text-color="#606266"
          active-text-color="#ffd04b"
        >
          <!-- 菜单颜色自行修改 -->
          <el-menu-item class="el-menu-item" index="1" style="font-size: 20px"
            >1</el-menu-item
          >
          <el-menu-item class="el-menu-item" index="2" style="font-size: 20px"
            >2</el-menu-item
          >
          <el-menu-item class="el-menu-item" index="3" style="font-size: 20px"
            >3</el-menu-item
          >
          <el-menu-item class="el-menu-item" index="4" style="font-size: 20px"
            >4</el-menu-item
          >
          <el-menu-item class="el-menu-item" index="5" style="font-size: 20px"
            >5</el-menu-item
          >
          <el-menu-item class="el-menu-item" index="6" style="font-size: 20px"
            >6</el-menu-item
          >
          <el-menu-item class="el-menu-item" index="7" style="font-size: 20px"
            >7</el-menu-item
          >
          <el-menu-item class="el-menu-item" index="8" style="font-size: 20px"
            >contact us</el-menu-item
          >
        </el-menu>
        <!-- 去官网看看怎么选择，，index的使用方法，还有其他种类的，自行更改吧 -->
      </el-header>

      <el-main class="el-main" style="height: 700px">
        <!-- 这里是搜索框和按钮，有一些用法，链接留给你了，可以自行删改，指路
        https://blog.csdn.net/qq_42268364/article/details/97375138?utm_term=elementui%E6%90%9C%E7%B4%A2%E6%A1%86&utm_medium=distribute.pc_aggpage_search_result.none-task-blog-2~all~sobaiduweb~default-5-97375138&spm=3001.4430
         -->
        <div class="logo">
          <img src="../assets/weblogo.png" />
        </div>
        <div class="search">
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
        <!-- introduction -->

        <div class="introduction">
          <span>Introduction</span>
          <el-divider></el-divider>
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
        <div class="banquan">&copy;版权所有BJTU</div>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "search",
  data() {
    //  搜索框
    return {
      diseaseList: [], //这个值是需要匹配的值
      disease: "", //这个值是用户正在输入的值
    };
  },
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
  background-color: #fff;
}
.el-menu-item {
  width: 12.5%;
}
.el-menu-demo {
  margin-top: 85px;
  margin-left: -20px;
  margin-right: -20px;
}
.inline-input {
  width: 50%;
}
.search {
  /* 搜索框和按钮的div */
  margin-top: 120px;
  height: 60px;
}

.signin {
  height: 60px;
}

.el-row {
  margin-bottom: 20px;
}
.el-col {
  border-radius: 4px;
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
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
.footer {
  padding: 15px;
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
/deep/.el-button {
  background-color: #102785;
  border-color: #102785;
}
.logo {
  margin-top: 60px;
  height: 50px;
  float: left;
  margin-left: 350px;
}
.introduction {
  margin-top: 80px;
  font-size: 30px;
  font-weight: 600;
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
