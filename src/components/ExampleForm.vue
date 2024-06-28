<script setup lang="ts">
import { ref } from 'vue'

const item = {
    date: '你说的对',
    name: '但爱莉希雅永远是我宝宝',
    address: '流萤宝宝也是'
}
const tableData = ref(Array.from({ length: 20 }).fill(item))
</script>

<template>
    <el-table :data="tableData" style="width: 100%">
        <el-table-column prop="date" label="Date" />
        <el-table-column prop="name" label="Name" />
        <el-table-column prop="address" label="Address" />
    </el-table>
</template>

<style scoped>
.example_form {
    padding: 0;
}
</style>
