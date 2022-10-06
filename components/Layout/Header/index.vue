<script lang="ts" setup>
const header = reactive({
  logo: 'https://cdn.jsdelivr.net/gh/novcu/picture/touxiang6.jpeg',
  twitter: '',
  github: 'https://github.com/LLiuHuan',
  weibo: '1',
  telegram: '1',
  mastodon: '',
  bilibili: '',
  rss: '',
  douban: '',
  zhihu: '',
})
</script>

<template>
  <header v-if="header" class="header">
    <div class="pt-70px hidden lg:block">
      <div class="content">
        <div class="h_frame pb-24px relative">
          <div class="text-center m-5px">
            <NuxtLink href="/">
              <img class="w-130px h-130px rounded-100px" style="display: initial" :src="header.logo" alt="logo">
            </NuxtLink>
          </div>
          <div class="text-center mx-24px mt-20px flex justify-center">
            <NuxtLink v-show="header.twitter" class="i-ri-twitter-fill mx-8px" rel="me" :href="header.twitter" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.github" class="i-ri-github-fill mx-8px" rel="me" :href="header.github" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.weibo" class="i-ri-weibo-fill mx-8px" rel="me" :href="header.weibo" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.telegram" class="i-ri-telegram-fill mx-8px" rel="me" :href="header.telegram" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.mastodon" class="i-ri-mastodon-fill mx-8px" rel="me" :href="header.mastodon" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.bilibili" class="i-ri-bilibili-fill mx-8px" rel="me" :href="header.bilibili" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.rss" class="i-ri-rss-fill mx-8px" rel="me" :href="header.rss" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.douban" class="i-ri-douban-fill mx-8px" rel="me" :href="header.douban" title="Mastodon" target="_blank" />
            <NuxtLink v-show="header.zhihu" class="i-ri-zhihu-line mx-8px" rel="me" :href="header.zhihu" title="Mastodon" target="_blank" />
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="less" scoped>
.header .h_frame:after {
  content: "";
  width: 100%;
  height: 1px;
  bottom: 2.5px;
  left: 0;
  position: absolute;
  //z-index: -2;
  background: -webkit-gradient(linear,left top,right top,color-stop(0%,#FFF),color-stop(35%,#eeeeee),color-stop(65%,#eeeeee),color-stop(100%,#FFF));
}

.dark .header .h_frame:after {
  background: -webkit-gradient(linear,left top,right top,color-stop(0%,#212429),color-stop(35%,#2b2e34),color-stop(65%,#2b2e34),color-stop(100%,#212429));
}
</style>
