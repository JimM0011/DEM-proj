<script setup>
import page_en from '../mds/md_en.mdx';
import page_ch from '../mds/md_ch.mdx';

// 设置一个变量来控制显示哪种语言的内容
import { ref } from 'vue';
const isEnglish = ref(true);

</script>

<template>
  <div>
    <el-divider />

    <!-- 设置一个可切换的语言选择器 -->
    <el-row justify="center" style="margin-bottom: 20px;">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
        <el-radio-group v-model="isEnglish">
          <el-radio-button 
            :label="true"
            @click="isEnglish = true"
          >
            English
          </el-radio-button>
          <el-radio-button 
            :label="false"
            @click="isEnglish = false"
          >
            中文
          </el-radio-button>
        </el-radio-group>
      </el-col>
    </el-row>

    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
            <page_en v-if="isEnglish" />
            <page_ch v-else />
        </el-col>
    </el-row>

  </div>
</template>