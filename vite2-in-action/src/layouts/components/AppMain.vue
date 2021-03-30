<template>
  <section class="app-main">
    <!-- 内部应该显示子路由页面信息 -->
    <transition mode='out-in'>
      <router-view/>
    </transition>
  </section>
</template>

<script>
export default {
  name: "AppMain",
};
</script>

<style scoped>
.app-main {
  /*50 = navbar  */
  min-height: calc(100vh - 50px);
  width: 100%;
  position: relative;
  overflow: hidden;
}
.tv-enter,
.v-leave-to {
  opacity: 0;
  transform: translateX(30px);
}
.v-enter-active,
.v-leave-active {
  transition: all 0.2s ease;
}

</style>
