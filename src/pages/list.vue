<template>
  <div>
    <h1>欢迎来到易师傅的列表页面</h1>

    <ListItem></ListItem>

    <input type="text" v-focus>
    <input type="text" value="value">

    <strong>
      姓名：{{ userInfo.userName }}
      性别：{{ userInfo.sex }}
    </strong>
  </div>
</template>

<script setup lang="ts">
import { useUserStore } from '@/stores/useUserStore'
const userInfo = useUserStore().userInfo
// console.log(userInfo);

</script>