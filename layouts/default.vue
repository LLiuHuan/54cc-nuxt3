<template>
  <div class="flex flex-col h-full dark:bg-[#232931] dark:text-[#aaa]">
    <LayoutHeader />
    <LayoutNavigation />

    <main class="">
      <slot />
    </main>
    <LayoutFooter />
    <Tools />
  </div>
</template>

<style lang="less">
@import url(./style/layout.module.less);
</style>
