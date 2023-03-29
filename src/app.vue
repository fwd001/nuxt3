<template>
  <div>
    <!-- 路由出口 -->
    <NuxtLayout>
      <NuxtPage></NuxtPage>
    </NuxtLayout>
  </div>
</template>
<script setup lang="ts">
import { useUserStore } from '@/stores/useUserStore'

const userInfo = useUserStore().userInfo
console.log('userInfo:::',userInfo);

const runtimeConfig = useRuntimeConfig()
console.log('runtimeConfig', runtimeConfig.public, runtimeConfig.app);

const appConfig = useAppConfig()
console.log('appConfig', appConfig);

</script>
<style lang="less">
.page-enter-active,
.page-leave-active {
  transition: all 0.4s;
}
.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(1rem);
}
</style>