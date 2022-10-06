<!--

导航条

-->
<script lang="ts" setup>
import MobileMenu from '~/components/MobileMenu.vue'
import Search from '~/components/Search.vue'
import { emitter } from '~/utils/bus'

const data = [{
  title: '首页',
  url: '/',
}, {
  title: '分类',
  url: '/category',
  children: [{
    title: '前端',
    url: '/category/前端',
  }, {
    title: '后端',
    url: '/category/后端',
  }, {
    title: '数据库',
    url: '/category/数据库',
  }, {
    title: '运维',
    url: '/category/运维',
  }, {
    title: '其他',
    url: '/category/其他',
  }],
}, {
  title: '归档',
  url: '/archives',
}, {
  title: '标签',
  url: '/tags',
}, {
  title: '关于',
  url: '/about',
}, {
  title: '友链',
  url: '/links',
},
]

const title = '象笔记'
const isHeader = true
const search_show = () => {
  emitter.emit('search_show')
}

const mobile_show = () => {
  emitter.emit('mobile_show')
}

emitter.on('search', (value) => {
  console.log(value)
})
</script>

<template>
  <!-- pc 导航条 -->
  <div class="border-b-1 border-[#eee] sticky top-0 bg-#fff pt-8px pb-10px z-100 dark:bg-[#232931] dark:border-[#2b2e34]">
    <div class="content">
      <div class="relative font-medium flex justify-between">
        <div class="web_name float-left text-18px font-500 text-#000 dark:text-[#aaa] pt-8px pb-6px hidden lg:block" :class="{ no_headertop_pic: !isHeader }">
          <NuxtLink href="/" class="flex justify-center items-center">
            {{ title }} &nbsp;<span class="spot" />
          </NuxtLink>
        </div>
        <div class="h-50px float-left block lg:hidden" :class="{ no_headertop_img: !isHeader }">
          <NuxtLink href="/">
            <img class="h-full rounded-100%" src="https://cdn.jsdelivr.net/gh/novcu/picture/touxiang6.jpeg" alt="logo">
          </NuxtLink>
        </div>

        <div class="float-left pc_menu  flex items-center">
          <ul class="p-0 m-0 float-left hidden lg:block" style="list-style: none;">
            <li v-for="item in data" :key="item.url" class="float-left relative leading-1.7em pc_menu_li" :class="{ level: item.children }" style="list-style: none;">
              <NuxtLink class="text-12.5px py-7px px-12px text-#525252 dark:text-[#aaa] tracking-0.6px uppercase block relative" :to="item.url" exact-active-class="current">
                {{ item.title }}
              </NuxtLink>
            </li>
          </ul>
          <div class="float-right mr-5px cursor-pointer px-10px">
            <div class="i-ri-search-2-line h-39px w-0.9em text-xl" @click="search_show" />
          </div>

          <div class="block lg:hidden float-right">
            <div class="i-ri-apps-2-line h-39px w-1.2em" @click="mobile_show" />
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- pc 导航条 结束 -->

  <!-- pc 搜索框 -->
  <Search />
  <!-- 手机菜单 -->
  <MobileMenu :data="data" />
</template>

<style lang="less" scoped>
@import url(./index.module.less);

.navigation {
  border-bottom: 1px solid #eee;
  position: sticky;
  top: 0;
  background-color: #FFF;
  padding: 8px 0 10px 0;
  z-index: 100;
}

.pc_menu_li:hover::after {
  content: "";
  position: absolute;
  background: #000;
  left: 0;
  right: 0;
  bottom: 0px;
  width: 4px;
  height: 4px;
  border-radius: 10px;
  margin: 0 auto;
  opacity: 1;
}

.pc_menu .router-link-active:after {
  content: "";
  position: absolute;
  background: #f12349;
  left: 0;
  right: 0;
  bottom: 0px;
  width: 4px;
  height: 4px;
  border-radius: 10px;
  margin: 0 auto;
  opacity: 1;
}

.pc_menu .router-link-active a {
  color: #000;
}

// 带子菜单的
.submenu_ul {
  position: absolute;
  padding: 0.5rem .625rem;
  background: #FFF;
  border-radius: 4px;
  z-index: 99;
  box-shadow: 0px 0px 20px -5px rgb(158 158 158 / 22%);
  transition: all .5s ease-in-out;
  display: block !important;
  min-width: 5.62rem;
  left: -20px;
  opacity: 0;
  visibility: hidden;
}

.submenu_li {
  list-style: none;
  line-height: 2.187rem;
  text-align: center;
}

.submenu_li a {
  padding: 0 !important;
}

.submenu_li::after,.submenu_li::after,.submenu_li a::after {
  display: none;
}

.level:hover .submenu_ul {
  visibility: visible;
  opacity: 1;
}
</style>
