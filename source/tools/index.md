---
title: 我的百宝箱
date: 2025-12-21
comments: false
---

<!-- 这里是 CSS 样式区，控制卡片长什么样 -->
<style>
  .tool-group {
    display: flex;
    flex-wrap: wrap;
    gap: 15px; /* 卡片之间的间距 */
    margin-bottom: 30px;
  }
  .tool-card {
    background: #f9f9f9; /* 卡片背景色 */
    border: 1px solid #e0e0e0;
    border-radius: 8px; /* 圆角 */
    padding: 15px;
    width: calc(33.33% - 10px); /* 一行放3个 */
    box-sizing: border-box;
    text-decoration: none !important; /* 去掉下划线 */
    color: #333 !important;
    transition: all 0.3s; /* 动画过渡 */
    display: flex;
    align-items: center;
  }
  /* 鼠标悬停时的特效 */
  .tool-card:hover {
    transform: translateY(-5px); /* 向上浮动 */
    box-shadow: 0 5px 15px rgba(0,0,0,0.1); /* 加阴影 */
    background: #fff;
    border-color: #3273dc; /* 边框变蓝 */
  }
  .tool-icon {
    width: 40px;
    height: 40px;
    margin-right: 15px;
    border-radius: 50%;
  }
  .tool-info {
    display: flex;
    flex-direction: column;
  }
  .tool-title {
    font-weight: bold;
    font-size: 16px;
    margin-bottom: 5px;
  }
  .tool-desc {
    font-size: 12px;
    color: #888;
  }
  /* 手机端适配：一行变一个 */
  @media (max-width: 768px) {
    .tool-card {
      width: 100%;
    }
  }
</style>

<!-- 下面是正文内容区 -->

## 🛠️ 常用效率
<div class="tool-group">
  <!-- 卡片 1：飞书 -->
  <a class="tool-card" href="https://www.feishu.cn/" target="_blank">
    <!-- 图标地址，可以直接用网上的图片 -->
    <img class="tool-icon" src="https://lf3-static.bytednsdoc.com/obj/eden-cn/pipieh7nupabozups/feishu_logo_2020.png">
    <div class="tool-info">
      <span class="tool-title">飞书文档</span>
      <span class="tool-desc">极致的协作办公体验</span>
    </div>
  </a>

  <!-- 卡片 2：ChatGPT -->
  <a class="tool-card" href="https://chat.openai.com/" target="_blank">
    <img class="tool-icon" src="https://upload.wikimedia.org/wikipedia/commons/0/04/ChatGPT_logo.svg">
    <div class="tool-info">
      <span class="tool-title">ChatGPT</span>
      <span class="tool-desc">最强 AI 助手</span>
    </div>
  </a>

   <!-- 卡片 3：复制这段代码增加新卡片 -->
  <a class="tool-card" href="https://www.remove.bg/zh" target="_blank">
    <img class="tool-icon" src="https://www.remove.bg/favicon.ico">
    <div class="tool-info">
      <span class="tool-title">Remove.bg</span>
      <span class="tool-desc">在线一键抠图</span>
    </div>
  </a>
</div>

## 🐟 摸鱼专区
<div class="tool-group">
  <!-- 卡片 4 -->
  <a class="tool-card" href="https://www.bilibili.com/" target="_blank">
    <img class="tool-icon" src="https://www.bilibili.com/favicon.ico">
    <div class="tool-info">
      <span class="tool-title">Bilibili</span>
      <span class="tool-desc">干杯 ( ゜- ゜)つロ</span>
    </div>
  </a>
</div>

## HIT专区
<div class="tool-group">
  <!-- 本科生院 -->
  <a class="tool-card" href="https://hituc.hit.edu.cn" target="_blank">
    <img class="tool-icon" src="https://upload.wikimedia.org/wikipedia/zh/thumb/4/46/Harbin_Institute_of_Technology_logo.svg/330px-Harbin_Institute_of_Technology_logo.svg.png">
    <div class="tool-info">
      <span class="tool-title">本科生院</span>
    </div>
  </a>

  <!-- 图书馆 -->
  <a class="tool-card" href="http://www.lib.hit.edu.cn" target="_blank">
    <img class="tool-icon" src="/img/tools/hit-lib-logo.jpg">
    <div class="tool-info">
      <span class="tool-title">校图书馆</span>
    </div>
  </a>
</div>