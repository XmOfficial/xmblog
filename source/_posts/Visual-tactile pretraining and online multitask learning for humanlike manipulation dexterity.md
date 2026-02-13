---
title: 视触觉预训练和多任务在线学习促进仿人操纵灵活性
katex: true
keywords: 111, 222
date: 2025-12-25 11:11:42
tags:
  - 机器人
categories:
  - SR
cover: img/SR/2026.1/cover1.png
banner:
  type: img
  bgurl: /img/banner_bg.jpg
  banner_text: Hi my new friend!
---


>笔者评价：
>
>能发SR的我没能力评价


文章标题：Visual-tactile pretraining and online multitask learning for humanlike manipulation dexterity
文章下载链接：https://xmofficial.lanzoub.com/iDbC43id9jkd
本文发布时间：2026-2-12

## 全文速览
实现对机械手的灵巧操控难点在于高维的动作-观测空间，复杂的接触动力学方程和摄像头被频繁地遮挡。为了解决这个问题，文章从人类对物体的观察方式学习当中获得灵感，并提出了一种新的学习框架。
![](1-2.jpg)

这种学习框架通过对人类演示的自我监督学习来学习视觉-触觉整合表征。将视觉与触觉解耦使得机器人可以仅通过单目图像和二值化接触信号来得到可行的操作策略。
为了验证该框架的效果，文章使用RL和线上模仿学习训练了多任务策略，并且使用该策略控制机器手完成了对5种可见物体的抓取，成功率达到85%。该策略还可以扩展到对受遮挡物体的抓取，不过这些任务与训练任务具有相似的坐标系位置。



---

## 当前存在的问题


## 解决方案


## 实验效果验证


## 结语