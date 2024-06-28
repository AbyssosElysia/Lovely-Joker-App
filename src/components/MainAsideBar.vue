<script setup lang="ts">
import { Menu as IconMenu, Compass } from '@element-plus/icons-vue'
</script>

<template>
    <el-aside class="MainAsideBar" width="200px">
        <el-scrollbar>
            <el-menu :default-openeds="['1', '2']">
                <el-sub-menu index="1">
                    <template #title>
                        <el-icon><compass /></el-icon>功能导航
                    </template>
                    <el-menu-item-group>
                        <el-menu-item index="1-1">用户管理</el-menu-item>
                        <el-menu-item index="1-2">组织管理</el-menu-item>
                        <el-menu-item index="1-3">行业动态管理</el-menu-item>
                        <el-menu-item index="1-4">课程管理</el-menu-item>
                        <el-menu-item index="1-5">会议管理</el-menu-item>
                        <el-menu-item index="1-6"></el-menu-item>
                    </el-menu-item-group>
                </el-sub-menu>
                <el-sub-menu index="2">
                    <template #title>
                        <el-icon><icon-menu /></el-icon>数据分析
                    </template>
                    <el-menu-item-group>
                        <el-menu-item index="2-1">用户行为数据分析</el-menu-item>
                        <el-menu-item index="2-2">性能分析</el-menu-item>
                    </el-menu-item-group>
                </el-sub-menu>
            </el-menu>
        </el-scrollbar>
    </el-aside>
</template>

<style scoped>
.MainAsideBar {
    color: var(--el-text-color-primary);
    background: var(--el-color-primary-light-8);
}
</style>
