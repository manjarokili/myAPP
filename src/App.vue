<template>
  <div id="app" class="app-container">
    <!-- 顶部Header区域 -->
    <mt-header fixed title="kilimanjaro"></mt-header>
    <!-- 中间路由router-view区域 -->
    <transition>
      <router-view></router-view>
    </transition>
    <!-- 底部Tabbar区域 -->
    
    <nav class="mui-bar mui-bar-tab">
      <router-link class="mui-tab-item" to="/home">
        <span class="mui-icon mui-icon-home"></span>
        <span class="mui-tab-label">首页</span>
      </router-link>

      <router-link class="mui-tab-item" to="/member">
        <span class="mui-icon mui-icon-contact">
          <span class="mui-badge">0</span></span>
        <span class="mui-tab-label">我的</span>
      </router-link>

      <router-link class="mui-tab-item" to="/shopcart">
        <span class="mui-icon mui-icon-videocam">
        </span>
        <span class="mui-tab-label">视频</span>
      </router-link>

      <router-link class="mui-tab-item" to="/search">
        <span class="mui-icon mui-icon-search"></span>
        <span class="mui-tab-label">搜索</span>
      </router-link>
    </nav>
  </div>
</template>

<style lang="scss" scoped>
.app-container {
  padding-top: 40px;
  overflow-x: hidden;
}
.mui-bar {
  background-color: aliceblue;
  box-shadow: none;
}
.mint-header {
  background-color: aliceblue;
  color: black;
}
.v-enter {
  opacity: 0;
  transform: translateX(100%);
}
.v-leave-to {
  transform: translateX(-100%);
  position: absolute;
}
.v-enter-active,
.v-leave-active {
  transition: all 0.2s ease;
}
</style>