<script setup lang="ts">
import { onLoad } from "@dcloudio/uni-app";
import { onUnmounted } from "vue";

onLoad(() => {
  console.log('wo detail onload');
})

onUnmounted(() => {
  console.log('detail onUnmounted');
})
</script>

<template>
  <view>workspace detail</view>
</template>

<style scoped></style>
