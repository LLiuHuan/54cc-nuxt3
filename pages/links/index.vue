<template>
  <div class="content mt-30px lg:mt-70px">
    <article>
      <div class="post_not">
        <h1 class="post_not_title">
          友链
        </h1>
        <div class="post_not_info">
          <time datetime="2021-04-19T16:45:00+08:00">2021-04-19</time><i class="iconfont icon-xiegangxian" /><span>12 字</span>
        </div>
      </div>

      <div class="post_bar">
        <div class="post_conter">
          <div class="song post">
            <h3>推荐链接</h3>
            <div class="links_list">
              <div class="links">
                <div class="links_box">
                  <a target="_blank" href="https://novcu.com"><div class="links_img"><img src="https://cdn.jsdelivr.net/gh/novcu/picture/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20201226145224.jpg"></div><div class="links_name">樗顾</div></a>
                </div>
              </div>
            </div>
            <h3>友情链接</h3>
            <div class="links_list">
              <div class="links">
                <div class="links_box">
                  <a target="_blank" href="https://novcu.com"><div class="links_img"><img src="https://cdn.jsdelivr.net/gh/novcu/picture/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20201226145224.jpg"></div><div class="links_name">樗顾</div></a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="post_tags">
        <a>aaaaaaaaaaavb</a>
      </div>
    </article>

    <div class="about_author">
      <div class="about_img">
        <img src="https://q.qlogo.cn/g?b=qq&amp;nk=184555556&amp;s=100">
      </div>
      <div class="about_info">
        <div class="about_name">
          admin
        </div>

        <div class="about_excerpt">
          aaaaaaaaaaaaaavas
        </div>
      </div>
      <div class="about_shang">
        <span onclick="reward()" class="shang_btn"><i class="iconfont icon-qianbao" />赞赏</span>
      </div>
    </div>

    <div class="reward_box">
      <input id="reward_weixin" type="radio" name="tab" class="reward_none" checked=""><input id="reward_zfb" type="radio" name="tab" class="reward_none"><div class="reward_title">
        感谢打赏
      </div><div class="reward_body">
        <div class="reward_body_weixin reward_none">
          <img src="<?php $this->options->微信打赏二维码(); ?>">
        </div><div class="reward_body_zfb reward_none">
          <img src="<?php $this->options->支付宝打赏二维码(); ?>">
        </div>
      </div><div class="reward_option">
        <div class="reward_ul">
          <label for="reward_weixin"><span class="reward_option_weixin">微信打赏</span></label><label for="reward_zfb"><span class="reward_option_zfb">支付宝打赏</span></label>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
@import "index.module.less";
</style>
