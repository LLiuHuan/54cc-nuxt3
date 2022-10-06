<script>
import ArticleHide from '../components/ArticleHide'
import ArticleLarge from '../components/ArticleLarge'
export default {
  components: { ArticleLarge, ArticleHide },
}
</script>

<template>
  <div class="content mt-30px lg:mt-70px">
    <!-- 隐藏图片 -->
    <ArticleHide />
    <!-- 小图 -->

    <!-- 大图 -->
    <article class="large_list" />
    <ArticleLarge />
    <ArticleHide />
  </div>
</template>

<style lang="less">
@import "index.module.less";
</style>
