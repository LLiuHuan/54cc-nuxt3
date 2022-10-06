<template>
  <article class="hide_list mb-35px pb-40px border-dotted border-b border-[#ddd] dark:border-[#777]">
    <div class="flex">
      <div class="float-lefr w-131px h-131px lg:w-180px lg:h-180px relative overflow-hidden flex-shrink-0">
        <div class="relative">
          <div class="hide_img w-full h-131px lg:h-180px translate-y-[-100%] duration-[0.35s] ease-in-out overflow-hidden absolute t-0 l-0 rounded-3px">
            <a href="https://ilcode.cn/archives/154/">
              <img class="duration-[0.8s] w-full h-full object-cover" data-ll-status="loaded" src="https://cdn.jsdelivr.net/gh/novcu/picture/touxiang6.jpeg"></a>
          </div>
        </div>
        <div class="absolute t-0 l-0 w-full transform-y-[0%] duration-[0.35s] ease-in-out hide_pic">
          <div class="p-0 lg:py-15.5px text-center">
            <div class="text-65px mb-10px lg:text-85px font-bold lg:mb-20px">
              01
            </div>
            <div class="text-13px">
              Oct
            </div>
          </div>
        </div>
      </div>
      <div class="ml-20px flex flex-col flex-1 text-left">
        <div class="flex-1" style="-ms-flex:1 1 auto">
          <h2 class="mb-0 mt-0 text-20px overflow-hidden" style="display:-webkit-box;-webkit-line-clamp:1;-webkit-box-orient:vertical;">
            <span class="index_top">置顶</span>
            <NuxtLink class="duration-[0.35s] ease-in-out hover:!text-[#f12349]" href="https://ilcode.cn/archives/154/">
              新增column属性及瀑布流布局
            </NuxtLink>
          </h2>
          <div class="text-14px text-[#969fb7] mt-15px">
            In&nbsp;
            <span class="text-[#454b58]">
              <a href="https://ilcode.cn/category/code/">编程</a>
            </span>&nbsp;at
            <time class="text-[#454b58]" datetime="2022-10-01T15:09:40+08:00">2022-10-01</time>
          </div>
          <div class="mt-14px text-15px leading-26px overflow-hidden line-clamp-1 lg:line-clamp-3" style="display:-webkit-box;-webkit-box-orient:vertical;">
            column列布局新增的column属性用来进行多列布局。注意新增属性需要些兼容前缀，如-moz-和-webkit- ，最大兼容到IE10column-count     把当前div中的文本/元素划分为三列-moz-column-c...
          </div>
        </div>
        <div class="hide_foot mt-15px flex justify-between">
          <span class="text-14px font-semibold flex items-center hover:text-[#f12349] duration-[0.35s] ease-in-out">
            <NuxtLink class="hover:!mr-3px duration-[0.35s] ease-in-out" href="https://ilcode.cn/archives/154/">Read more</NuxtLink>
            &nbsp;
            <svg class="i-ri-arrow-right-line w-20px h-20px" />
          </span>
          <span class="text-13px font-semibold flex items-center">
            <!-- 评论 -->
            <svg class="i-ri-message-3-line" />&nbsp;0
          </span>
        </div>
      </div>
    </div>
  </article>
</template>
