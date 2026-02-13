---
title: SR 2026.1 Summary
date: 2026-02-03 18:30:33
tags:
  - Science Robotics
  - Robotics
categories:
  - Science Robotics 分析
cover: /img/SR/2026.1/sr2026.1-cover.jpg
banner:
  type: img
  bgurl: /img/SR/banner_bg.jpg
  banner_text: Hi my new friend!

# 生成目录
toc:
  enable: true
  list_number: true
  post_title: false
  max_depth: 3
  min_depth: 1

---
2026 年 1 月

封面图（有点吓人，怎么新年第一期就这么抽象啊）

# FOCUS

## 1.Is intermittent swimming lazy or clever?
本文以“间歇式游动到底是偷懒还是聪明策略”为切入点，借助斑马鱼启发的机器人平台，从能耗、电功率与推进效率的角度解释间歇游动可能带来的优势与权衡。核心观点是，用机器人可测、可控的动力系统去拆解“爆发—滑行”相对连续摆动在效率与任务表现上的差异，从而为理解真实鱼类与仿生水下机器人的运动策略提供机制层面的依据。


## 2.Within arm’s reach: A path forward for robot dexterity
本文围绕“机器人灵巧手”如何跨越从演示到真实环境的落差展开，强调人类在视觉与触觉的融合上具有天然优势，并指出利用人类数据进行视触觉预训练，可以显著提升在仿真中训练出的操作策略的稳健性与可迁移性。文章更像路线图和观点综述，聚焦数据、感知表征与训练范式如何共同推动可泛化的灵巧操作，而不仅是堆叠更复杂的硬件。

# Research Article

## 1.(FOCUS 1) Energy efficiency and neural control of continuous versus intermittent swimming in a fishlike robot
本文以鱼形机器人为实验载体，对比“连续游动”与“间歇游动”的能量效率与控制策略差异，并将神经控制、生物启发控制思路引入机器人游动的生成与调参；文章从仿生机器人作为“可重复、可测量的生物学工具”的角度出发，围绕间歇式运动中主动推进与被动滑行的组合，讨论其在能耗、姿态/轨迹可控性以及可能的生物学解释上的取舍，为水下仿生机器人设计与动物运动机理研究提供量化对照。

## 2.(FOCUS 2) Visual-tactile pretraining and online multitask learning for humanlike manipulation dexterity
本文聚焦多指灵巧操作的核心瓶颈：精细手指协同难、对任务变化敏感、真实机器人数据采集成本高；作者提出结合“视觉-触觉预训练”与“在线多任务学习”的框架，利用更通用的感知表征与跨任务共享能力来提升策略学习效率与泛化性，并在操作过程中通过在线学习适应不同任务/目标，旨在更接近人类式的灵巧与流畅操控。

## 3.(COVER) Learning realistic lip motions for humanoid face robots
本文关注人形机器人面部中“唇部运动”的关键性：在人机对话里，唇形与语音同步以及细节真实感会显著影响理解与信任.作者提出一种学习驱动的唇部运动生成、控制方法，使机器人能够更逼真地生成与语音对应的口型变化，并面向实时交互场景优化稳定性与自然度，从而提升类人面部机器人的沟通表现与社会可接受度。

## 4. Autonomous robotic intraocular surgery for targeted retinal injections
本文面向眼内手术这一高精度、强约束场景，指出其主要难点在于视野受限、组织与器械的深度感知困难、操作容错极低；作者提出自主/半自主的机器人眼内操作方案，围绕“目标视网膜注射”任务，在环境感知、深度估计与运动控制（以及由此带来的精度与安全边界）上做系统化设计，目标是提升注射定位的可重复性与稳定性，并为更高等级的手术自动化奠定基础。

## 5. Architectural swarms for responsive façades and creative expression
本文把群体机器人引入建筑立面与创意表达场景，借鉴蜂巢、蚁桥等“活体结构”通过自组织持续适应环境的机制，提出由大量个体代理协同形成可变形、可响应的立面系统；研究重点在于群体规则、结构/外观变化与环境/使用者需求之间的映射关系，展示“动态、可重构、具表现力”的建筑外表皮如何通过群体智能实现，而不仅是传统静态构件的被动调节。


