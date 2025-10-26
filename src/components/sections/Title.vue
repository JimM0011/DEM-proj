<script lang="ts" setup>

import { ElIcon } from 'element-plus'
import { Document, Files, MagicStick, Picture, DataAnalysis, Film } from '@element-plus/icons-vue'

// 按钮颜色
const btn_color = '#444444'

// 提供引导资料链接
const buttons = [
  {
    disabled: true,
    name: "Paper",
    component: Document,
  },
  {
    disabled: true,
    name: "Code",
    // link: "https://github.com/JunyaoHu/academic-project-page-template-vue",
    component: Files,
  },
  {
    disabled: true,
    name: "Poster",
    component: Picture,
  },
  {
    disabled: true,
    name: "Video",
    // link: "https://www.bilibili.com/video/BV15XkgYiE73/",
    component: Film,
  },
  {
    disabled: true,
    name: "Slide",
    component: DataAnalysis,
  },
]

</script>

<template>
  <div>

    <!-- 最新消息提示 -->
    <el-row justify="center">
      <el-col :span="24">
        <el-alert title="🔥 This page is still under development." type="success" />
      </el-col>
    </el-row>

    <!-- 文章标题 -->
    <el-row justify="center">
      <el-col :span="20">
        <h1 class="paper-title">
          <span :style="{color:'#000000'}">
            Decoupled Entropy Minimization
          </span>
        </h1>
      </el-col>
    </el-row>

    <!-- 作者名单 -->
    <el-row justify="center">
      <a 
        href="https://jimm0011.github.io/"
        target="_blank"
      >
        <el-button class="title-button" type="primary" text>
          <span class="author">
            Jing Ma<sup class="name_sup">1,*</sup>
          </span>
        </el-button>
      </a>
      <a 
        href="https://vain222.github.io/#/"
        target="_blank"
      >
        <el-button class="title-button" type="primary" text>
          <span class="author">
            Hanlin Li<sup class="name_sup">1,*</sup>
          </span>
        </el-button>
      </a>
      <a 
        href="https://eglxiang.github.io/"
        target="_blank"
      >
        <el-button class="title-button" type="primary" text>
          <span class="author">
            Xiang Xiang<sup class="name_sup">1,*#</sup>
          </span>
        </el-button>
      </a>
    </el-row>

    <!-- 地址名单 -->
    <el-row justify="center">
      <a
        href="https://www.hust.edu.cn/"
        target="_blank"
      >
        <el-button class="title-button" type="primary" text>
          <span class="address">
            <sup class="address_sup">1</sup>Huazhong University of Science and Technology (HUST)
          </span>
        </el-button>
      </a>
    </el-row>

    <!-- 共一和通讯提示内容 -->
    <el-row justify="center" class="con-cor">
        *: Equal Contribution. #: Corresponding Author.
    </el-row>


    <!-- 提供引导按钮 -->
    <el-row justify="center" style="margin-bottom: 20px;">
      <el-col :span="20">
        <el-row justify="center">
          <a :href=button.link v-for="button in buttons">
            <el-button class="guidance-button" size="default" :color="btn_color" :disabled="button.disabled" round>
              <el-icon :size="18">
                <component :is="button.component" />
              </el-icon>
              <span class="btn-text">{{ button.name }}</span>
            </el-button>
          </a>
        </el-row>
      </el-col>
    </el-row>

  </div>
</template>

<style scoped>

/* 文章标题字体、字间距、居中排布、字号 */
.paper-title {
  font-family: "MyFont", Verdana, sans-serif;
  letter-spacing: 2px;
  font-size: 42px;
  margin: 32px;
  text-align: center;
}

/* 姓名和地址按钮 */
.title-button {
  margin: 10px 3px;
}

/* 姓名和地址按钮光标悬浮 */
.title-button:hover {
  margin: 10px 8px;
}

/* 引导材料按钮 */
.guidance-button {
  margin: 8px 5px;
  box-shadow: #d8d8d8 1px 1px 1px 1px;
}

/* 姓名属性 */
.author {
  font-size: 18px;
  margin-left: 3px;
}

/* 姓名上标属性 */
.name_sup {
  color: #606266; 
  margin-left: 3px;
}

/* 地址属性 */
.address {
  font-size: 18px;
}

/* 地址上标属性 */
.address_sup {
  color: #606266; 
  margin-right: 1px;
}

/* 头像属性 */
.el-avatar {
  margin-right: 6px;
  box-shadow: #b7b7b7 0px 0px 3px 1px;
}

/* 共一和通讯文字属性 */
.con-cor {
  font-family: Arial;
  font-size: 14px;
  margin: 18px 0px;
  text-align: center;
}

/* 强调信息属性 */
.emphasis {
  color: chocolate;
  font-weight: bold;
  margin: 8px;
  font-size: 22px;
  text-align: center;
}

/* 引导材料按钮文字属性 */
.btn-text {
  font-size: 18px;
  color: #ffffff;
}

.el-alert {
  margin: 10px 0 0;
}

.el-alert:first-child {
  margin: 0;
}

.logo {
  width: 150px; 
  height: 150px;
  border-radius: 50%;
  box-shadow: #ced3dc 0px 0px 3px 2px;
  margin-top: 40px;
}

/* 手机端链接样式处理 */
a:-webkit-any-link {
  text-decoration: none;
}

/* 取消鼠标焦点悬浮在链接上的颜色装饰 */
a:hover {
  color: inherit;
  border-bottom: none;
}

/* 链接装饰，取消下划线和链接颜色 */
a {
	text-decoration: None;
	color: inherit;
}

</style>