<template>
  <div>
    <el-scrollbar wrap-class="scrollbar-wrapper">
      <el-menu
        mode="vertical"
        :default-active="1"
        :collapse="false"
        :background-color="menuBg"
        :text-color="menuText"
        :unique-opened="false"
        :active-text-color="menuActiveText"
        :collapse-transition="false"
      >
        <el-menu-item index="2">
          <i class="el-icon-menu"></i>
          <template #title>导航二</template>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-setting"></i>
          <template #title>导航四</template>
        </el-menu-item>
      </el-menu>
    </el-scrollbar>
  </div>
</template>
<script>
/* eslint-disable */
import { computed, toRefs } from 'vue'
import variables from '@/styles/variables.scss'

export default {
  name: 'Sidebar',
  setup () {
    const variables = computed(() => {
      return variables
    })

    const { menuBg, menuText, menuActiveText } = toRefs(variables)

    return {
      menuBg,
      menuText,
      menuActiveText
    }
  }
}
</script>
<style lang="scss" scoped>
</style>
