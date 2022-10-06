<template>
  <article class="hide_list mb-35px pb-40px border-dotted border-b border-[#ddd] dark:border-[#777]">
    <div class="mb-24px">
      <div class="w-full h-152px lg:h-381px overflow-hidden rounded-3px">
        <NuxtLink href="/article/5">
          <img class="hover:scale-110 w-full h-full object-cover rounded-3px duration-[0.8s]" data-ll-status="loaded" src="https://cdn.jsdelivr.net/gh/novcu/picture/touxiang6.jpeg">
        </NuxtLink>
      </div>
    </div>
    <div class="index_bg_info">
      <div class="flex">
        <div class="float-left py-0 px-30px lg:py-5.5px lg:px-35px text-center w-131px lg:w-180px">
          <div class="text-60px lg:text-80px font-bold mb-20px">
            03
          </div>
          <div class="text-13px">
            Oct
          </div>
        </div>

        <div class="ml-10px lg:ml-20px flex flex-col flex-1 index_list_post">
          <div class="index_list_body flex-1">
            <h2 class="my-0 text-18px lg:text-20px overflow-hidden" style="display:-webkit-box;-webkit-line-clamp:1;-webkit-box-orient:vertical;">
              <a href="http://82.157.65.212:8889/index.php/archives/5/">啊啊</a>
            </h2>

            <div class="mt-14px text-14px lg:text-15px  line-clamp-2 lg:line-clamp-3 leading-26px overflow-hidden" style="display:-webkit-box;-webkit-box-orient:vertical;">
              啊啊啊
            </div>
          </div>

          <div class="mt-15px flex justify-between">
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
    </div>
  </article>
</template>
