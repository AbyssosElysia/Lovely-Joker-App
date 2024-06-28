<script setup lang="ts">
import { Menu as Setting } from '@element-plus/icons-vue'
</script>

<template>
    <el-header class="el-header">
        <div class="left-content">流萤宝宝世界第一可爱</div>
        <div class="right-content">
            <el-dropdown>
                <el-icon style="margin-right: 8px; margin-top: 1px">
                    <setting />
                </el-icon>
                <template #dropdown>
                    <el-dropdown-menu>
                        <el-dropdown-item>你谁啊你敢点我?</el-dropdown-item>
                        <el-dropdown-item>信不信我报警了?</el-dropdown-item>
                        <el-dropdown-item>色狼啊!有坏蛋!!!</el-dropdown-item>
                    </el-dropdown-menu>
                </template>
            </el-dropdown>
            <div>我,就是欢愉!!!</div>
        </div>
    </el-header>
</template>

<style scoped>
.el-header {
    display: flex;
    flex-wrap: wrap;
    background-color: var(--el-color-primary-light-7);
    color: var(--el-text-color-primary);
}

.left-content {
    text-align: left;
    font-size: 32px;
    flex: 1;
    align-items: center;
}

.right-content {
    text-align: right;
    font-size: 18px;
    flex: 1;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

/*@media (max-width: 1024px) {
  .el-header {
    flex-direction: column;
    align-items: flex-start;
  }

  .right-content {
    justify-content: flex-start;
    margin-top: 10px;
  }
}*/
</style>
