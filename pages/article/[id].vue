<script lang="ts" setup>
const route = useRoute()
const type = route.params.id

console.log(type) // hello nuxt
</script>

<template>
  <div class="content mt-30px lg:mt-70px">
    <article class="posts">
      <!-- 无图样式 -->
      <div class="max-w-750px m-auto">
        <h1 class="my-0 text-28px font-medium">
          短代码演示
        </h1>
        <div class="text-14px mt-15px text-[#454b58] dark:text-[#777] flex items-center">
          <span>
            <NuxtLink class="hover:text-[#f12349] duration-[0.35s] ease-in-out" href="https://demo.novcu.com/magpie/index.php/category/default/">默认分类</NuxtLink>
          </span>
          <span class="text-[#f12349] text-18px mx-8px">/</span>
          <span>
            <time datetime="2021-04-19T16:40:47+08:00">2021-04-19</time>
            <span class="text-[#f12349] text-18px mx-8px">/</span>
            <span>198 字</span>
          </span>
        </div>
      </div>

      <div class="post_bar">
        <div class="post_leftbar">
          <ul class="post_leftbar_ul">
            <li class="post_leftbar_li">
              <button class="post_leftbar_dashang" onclick="weixin()">
                <i class="iconfont icon-weixin" />
              </button>
            </li>
            <li class="post_leftbar_li">
              <a href="#comments"><button class="post_leftbar_liuyan"><i class="iconfont icon-liuyan2" /></button></a>
            </li>
          </ul>
        </div>
        <div class="post_conter">
          <div class="text-15px text-justify text-[#0d131b] dark:text-[#aaa] mt-35px leading-1.8em tracking-0.013rem max-w-750px m-auto" style="word-wrap: break-word;">
            <ul>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
              <li>1</li>
            </ul>
          </div>
        </div>
        <!--        <div id="toc_container"> -->
        <!--          <div class="toc_container" style=""> -->
        <!--            <div class="inner-wrapper-sticky" style="position: relative; transform: translate3d(0px, 0px, 0px);"> -->
        <!--              <div id="TOC-text" class="TOC-text toc"> -->
        <!--                <ol class="toc-list "> -->
        <!--                  <li class="toc-list-item is-active-li"> -->
        <!--                    <a href="#坐而思不如起而行" class="toc-link node-name&#45;&#45;H3  is-active-link">坐而思不如起而行</a> -->
        <!--                  </li><li class="toc-list-item"> -->
        <!--                    <a href="#只想不做的人" class="toc-link node-name&#45;&#45;H3 ">只想不做的人</a> -->
        <!--                  </li><li class="toc-list-item"> -->
        <!--                    <a href="#避免“不为”成性" class="toc-link node-name&#45;&#45;H3 ">避免“不为”成性</a> -->
        <!--                  </li> -->
        <!--                </ol> -->
        <!--              </div> -->
        <!--            </div> -->
        <!--          </div> -->
        <!--        </div> -->
      </div>
      <div class="max-w-750px m-auto mt-15px text-14px">
        <a class="cursor-pointer mr-15px mb-10px border-b-1 border-[#b5b5b5] hover:border-[#f12349] border-dashed pb-5px hover:text-[#f12349] duration-[0.35s] ease-in-out">标签</a>
        <a class="cursor-pointer mr-15px mb-10px border-b-1 border-[#b5b5b5] hover:border-[#f12349] border-dashed pb-5px hover:text-[#f12349] duration-[0.35s] ease-in-out">标签</a>
        <a class="cursor-pointer mr-15px mb-10px border-b-1 border-[#b5b5b5] hover:border-[#f12349] border-dashed pb-5px hover:text-[#f12349] duration-[0.35s] ease-in-out">标签</a>
      </div>

      <!--      <div class="post_tool"> -->
      <!--        <div class="post_tool_zan"> -->
      <!--          <button id="agree-btn" class="zan_btn" type="button" data-action="like" data-id="12"> -->
      <!--            Enjoy<i class="agree-num">44</i> -->
      <!--          </button> -->
      <!--        </div> -->

      <!--        <div class="post_share"> -->
      <!--          <a class="weibo" href="//service.weibo.com/share/share.php?url=https://demo.novcu.com/magpie/index.php/archives/12/&amp;type=button&amp;language=zh_cn&amp;title=短代码演示" target="_blank"><i class="iconfont icon-weibo" /></a> -->
      <!--          <a class="ttww" href="https://twitter.com/intent/tweet?url=https://demo.novcu.com/magpie/index.php/archives/12/" target="_blank"><i class="iconfont icon-ttww" /></a> -->
      <!--          <a class="kongjiang" href="https://connect.qq.com/widget/shareqq/index.html?url=https://demo.novcu.com/magpie/index.php/archives/12/&amp;title=短代码演示" target="_blank"><i class="iconfont icon-QQ" /></a> -->
      <!--          <a class="weixin" onclick="weixin()" href="javascript:;"><i class="iconfont icon-weixin" /></a> -->
      <!--        </div> -->
      <!--      </div> -->
    </article>
  </div>
</template>

<style lang="less" scoped>
@import "index.module.less";
</style>
