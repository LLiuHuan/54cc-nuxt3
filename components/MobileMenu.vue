<script lang="ts" setup>
import { emitter } from '~/utils/bus'

interface Props {
  data: object
}

const props = defineProps<Props>()
const visible = ref(false)
const router = useRouter()

const close_menu = () => {
  visible.value = false
}

const routerPush = (url: string) => {
  router.push(url)
  close_menu()
}

emitter.on('mobile_show', () => {
  visible.value = true
})
</script>

<template>
  <div class="mobile" :class="{ mobile_open: visible }">
    <div class="mobile_info">
      <div class="mobile_img">
        <img src="https://q.qlogo.cn/g?b=qq&nk=37723657&s=100" alt="">
      </div>
      <div class="mobile_name">
        TTTLE <span class="h_spot" />
      </div>
    </div>

    <div class="mobile_meun">
      <ul class="mobile_ul">
        <li v-for="item in data" :key="item.url" class="mobile_li" :class="{ mobile_level: item.children }">
          <span @click="routerPush(item.url)">
            {{ item.title }}
          </span>
        </li>
      </ul>
    </div>
  </div>

  <!-- 磨砂背景 -->
  <div class="sap_mask mobile_mask" :class="{ sap_open: visible }" @click="close_menu()" />
</template>

<style lang="less" scoped>
.mobile {
  left:-300px;
  box-shadow:5px 0px 36px rgb(0 0 0 / 10%);
  z-index:9999;
  width:280px;
  position:fixed;
  top:0;
  bottom:0;
  background:#FFF;
  transition:all 0.35s ease-in-out;
  overflow-y:auto;
}
.mobile_open {
  left:0px;
}
.mobile_info {
  padding:20px;
  border-bottom:1px #e9ecef solid;
  text-align:center;
}
.mobile_img {
  max-width:60px;
  margin:0 auto;
  margin-bottom:15px;
}
.mobile_img img {
  width:100%;
  height:100%;
  border-radius:100%;
}
.mobile_name {
  font-size:16px;
  font-weight:600;
}
.mobile_name .h_spot {
  font-size:27px;
  display:inline-block;
  width:5px;
  height:5px;
  border-radius:50%;
  background-color:#ff374a;
  margin-left:3px;
}
.mobile_meun {
  padding:20px;
  font-size:14px;
}
.mobile_level i {
  float:right;
  font-weight:600;
  line-height:19px;
  color:#ff374a;
  font-size:14px;
}
.mobile_ul,.mobile_level_ul {
  padding:0;
  margin:0;
  list-style:none;
}
.mobile_level_ul {
  margin-top:15px;
  display:none;
}
.mobile_level_none {
  display:none;
}
.mobile_li {
  padding:10px 0;
}
.mobile_li a {
  width:100%;
}
.mobile_level_li {
  padding:5px 10px;
}
.mobile_footer {
  position:absolute;
  bottom:0;
  width:100%;
  padding:15px 20px;
  border-top:1px #e9ecef solid;
}
</style>
