<template>
  <view class="content">
    <image class="logo" src="/static/logo.png" />
    <view class="text-area">
      <text class="title">{{ title }}</text>
    </view>
    <view>
      <navigator url="/pages/workspace-detail/index?foo=abc&num=3" open-type="navigate">wo detail</navigator>
      <navigator url="/pages/user-profile/index" open-type="navigate">user profile</navigator>
    </view>
    <view>
      <input class="uni-input" focus placeholder="自动获得焦点" v-model="title" />
      <input type="text">
    </view>
    <view>
      <tui-button>页面主操作</tui-button>
    </view>
    <uni-card title="基础卡片" extra="额外信息">
				<text class="uni-body">这是一个基础卡片示例，此示例展示了一个标题加标题额外信息的标准卡片。</text>
			</uni-card>
  </view>
</template>

<script setup lang="ts">
import { onHide, onShow } from '@dcloudio/uni-app';
import { onUnmounted } from 'vue';
import { ref } from 'vue'
const title = ref('Hello')

onShow(() => {
  console.log('index onshow');
  const page = getCurrentPages()
})
onHide(() => {
  console.log('index onhide');
})
onUnmounted(() => {
  console.log('index unmounted');
})
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin-top: 200rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50rpx;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}

.uni-input {
  border: 1px solid red;
}
input {
  background-color: aqua;
}
</style>
