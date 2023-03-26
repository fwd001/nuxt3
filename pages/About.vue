<template>
  <div>aaa <span style="background-color: blue;">{{ msg }}</span></div>
  <button @click="goBack">返回</button>
</template>

<script setup lang="ts">
const msg = ref("message");
const router = useRouter()
function goBack() {
  router.back()
}
</script>
<style scoped>
div {
  background-color: #ccc;
}
</style>
