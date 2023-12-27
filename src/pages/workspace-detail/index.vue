<script setup lang="ts">
import { onLoad } from "@dcloudio/uni-app";
import { getCurrentInstance } from "vue";
import { onUnmounted } from "vue";

onLoad((options) => {
  // options 中能取到 query 信息
  console.log('wo detail onload', options);

  // vm 中也能取到，不建议
  const page = getCurrentPages()[0]
  console.log(page.$vm!.$route);
  
})

onUnmounted(() => {
  console.log('detail onUnmounted');
})
</script>

<template>
  <view>workspace detail</view>
</template>

<style scoped></style>
