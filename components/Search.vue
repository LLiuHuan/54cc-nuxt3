<script lang="ts" setup>
// 是否打开搜索框
import { emitter } from '~/utils/bus'

const visible = ref(false)
const searchValue = ref('')

emitter.on('search_show', () => {
  visible.value = true
})

const close_search = () => {
  visible.value = false
  searchValue.value = ''
}

const search = () => {
  emitter.emit('search', searchValue.value)
}
</script>

<template>
  <div class="search_bar h-180px lg:h-270px" :class="{ search_open: visible }">
    <div class="search_off hidden lg:block">
      <span @click="close_search"><i class="iconfont i-ri-close-fill" /></span>
    </div>
    <div class="search_box content mt-50px lg:mt-0">
      <div class="flex justify-center items-center cursor-pointer">
        <input v-model="searchValue" type="text" class="text" size="32" placeholder="搜索" @keyup.enter="search">
        <span class="i-ri-search-line" @click="search" />
      </div>
    </div>
    <div class="search_phone_off block lg:hidden">
      <span @click="close_search">
        <svg class="i-ri-close-fill w-18px h-18px inline" />
      </span>
    </div>
  </div>

  <div class="sap_mask search_mask" :class="{ sap_open: visible }" @click="visible = !visible" />
</template>

<style lang="less" scoped>
.search_bar {
  background-color:#FFF;
  position:fixed;
  width:100%;
  z-index:1000;
  top:-320px;
  transition:all 0.3s ease-in-out;
}

.search_open {
  top:0 !important;
}

.search_off {
  text-align:right;
}
.search_off span {
  cursor:pointer;
}
.search_off i {
  line-height:6.25rem;
  padding:0 3.125rem;
  font-size:1.125rem;
  color:#101010;
}
.search_box {
  position:relative;
}
.search_box .text {
  width:100%;
  border:none;
  border-bottom:1px solid #e6e6e6;
  outline:0;
  background-color:transparent;
  font-size:15px;
  padding:.9375rem 3.125rem .9375rem 0;
}
.search_box .submit {
  position:absolute;
  top:0;
  right:0;
  bottom:0;
  margin:0;
  padding:0;
  cursor:pointer;
  border:none;
  background:0 0;
  color:#101010;
}
.search_box .submit i {
  font-size:1.25rem;
}

.search_phone_off {
  position:absolute;
  bottom:-40px;
  width:100%;
  right:auto;
  top:auto;
  text-align:center;
}
.search_phone_off span {
  cursor:pointer;
  border:none;
  background:#FFF;
  border-radius:100px;
  padding:12px;
  font-size:12px;
}
</style>
