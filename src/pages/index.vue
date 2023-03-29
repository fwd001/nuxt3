<template>
  <div>
    <h1>欢迎来到nuxt的第一个页面</h1>
    <NuxtLink to="/list">进入列表页===={{ msg }}</NuxtLink>

    <br>
    <br>
    <div>fetch: {{ data }}</div>
    <div>
    {{ pending ? 'Loading' : count }}
  </div>
  <button @click="refresh">Refresh</button>
    <NuxtLink to="/user-admin/111">进入管理员 id 为 111 的用户中心</NuxtLink>
    
  </div>
</template>

<script setup>
const foo = useFoo()
console.log('foo:::', foo.value);
const msg = ref('massage1111')
const { data } = await useAsyncData('count1', () => $fetch('/api/count'))
const { pending, data: count } = useLazyAsyncData('count2', () => $fetch('/api/count'))
const refresh = () => refreshNuxtData('count2')
</script>