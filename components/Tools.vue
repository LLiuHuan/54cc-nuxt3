<script lang="ts" setup>
// const showTopTo = ref(false)
const color = useColorMode()
const showTopTo = useState('showTopTo', () => false)

const scrollToTop = () => {
  const scrollTop
      = window.pageYOffset
      || document.documentElement.scrollTop
      || document.body.scrollTop
  // that.scrollTop = scrollTop
  showTopTo.value = scrollTop > 350
}

const backTop = () => {
  const timer = setInterval(() => {
    const osTop
        = document.documentElement.scrollTop || document.body.scrollTop
    const ispeed = Math.floor(-osTop / 5)
    document.documentElement.scrollTop = document.body.scrollTop
        = osTop + ispeed
    if (osTop === 0)
      clearInterval(timer)
  }, 15)
}

function toggleDark() {
  color.preference = color.value === 'dark' ? 'light' : 'dark'
}

onMounted(() => {
  window.addEventListener('scroll', scrollToTop)
})
</script>

<template>
  <div class="fixed bottom-100px right-30px z-99 font-300">
    <div class="" style="list-style: none;">
      <span @click="toggleDark">切换主题</span>
    </div>
    <div v-if="showTopTo" id="top_to" class="mt-15px" style="">
      <!--      <a href="#"><button>返回顶部</button></a> -->
      <button @click="backTop">
        返回顶部
      </button>
    </div>
  </div>
</template>
