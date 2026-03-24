---
title: md与html对照表
date: 2026-03-24 11:06:21
tags:
---

## 1）标题

```md
# 一级标题
## 二级标题
### 三级标题
```

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
```

---

## 2）段落、换行、空行

### Markdown

```md
这是第一段。

这是第二段。

这是第一行  
这是第二行
```

### HTML

```html
<p>这是第一段。</p>
<p>这是第二段。</p>
<p>这是第一行<br>这是第二行</p>
```

---

## 3）粗体、斜体、删除线

```md
**加粗**
*斜体*
***加粗斜体***
~~删除线~~
```

```html
<strong>加粗</strong>
<em>斜体</em>
<strong><em>加粗斜体</em></strong>
<del>删除线</del>
```

---

## 4）引用

```md
> 这是一段引用
>> 这是二级引用
```

```html
<blockquote>
  这是一段引用
  <blockquote>这是二级引用</blockquote>
</blockquote>
```

---

## 5）无序列表

```md
- 苹果
- 香蕉
  - 小香蕉
  - 大香蕉
- 橙子
```

```html
<ul>
  <li>苹果</li>
  <li>香蕉
    <ul>
      <li>小香蕉</li>
      <li>大香蕉</li>
    </ul>
  </li>
  <li>橙子</li>
</ul>
```

---

## 6）有序列表

```md
1. 打开编辑器
2. 写内容
3. 保存文件
```

```html
<ol>
  <li>打开编辑器</li>
  <li>写内容</li>
  <li>保存文件</li>
</ol>
```

---

## 7）任务列表

```md
- [x] 已完成
- [ ] 未完成
```

```html
<ul>
  <li><input type="checkbox" checked> 已完成</li>
  <li><input type="checkbox"> 未完成</li>
</ul>
```

---

## 8）链接

```md
[OpenAI](https://openai.com)
```

```html
<a href="https://openai.com">OpenAI</a>
```

### 新标签打开

```html
<a href="https://openai.com" target="_blank" rel="noopener noreferrer">OpenAI</a>
```

---

## 9）图片

```md
![示例图片](https://example.com/image.png)
```

```html
<img src="https://example.com/image.png" alt="示例图片">
```

### 设置宽度

```html
<img src="https://example.com/image.png" alt="示例图片" width="300">
```

### 居中图片

```html
<p align="center">
  <img src="https://example.com/image.png" alt="示例图片" width="300">
</p>
```

---

## 10）行内代码和代码块

### 行内代码

```md
这里有一个 `console.log()` 示例
```

```html
这里有一个 <code>console.log()</code> 示例
```

### 代码块

````md
```js
console.log("hello");
```
````

```html
<pre><code>console.log("hello");</code></pre>
```

---

## 11）分隔线

```md
---
```

```html
<hr>
```

---

## 12）表格

```md
| 姓名 | 年龄 | 城市 |
|---|---:|:---:|
| 张三 | 18 | 北京 |
| 李四 | 20 | 上海 |
```

```html
<table>
  <thead>
    <tr>
      <th>姓名</th>
      <th align="right">年龄</th>
      <th align="center">城市</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>张三</td>
      <td align="right">18</td>
      <td align="center">北京</td>
    </tr>
    <tr>
      <td>李四</td>
      <td align="right">20</td>
      <td align="center">上海</td>
    </tr>
  </tbody>
</table>
```

---

# Markdown + HTML 混写高频用法

## 13）文字颜色

Markdown 原生不支持文字颜色，可以混写 HTML：

```md
这是普通文字，<span style="color:red;">这是红色文字</span>
```

```html
这是普通文字，<span style="color:red;">这是红色文字</span>
```

---

## 14）文字大小

```md
普通文字  
<span style="font-size: 20px;">大号文字</span>
```

---

## 15）高亮

有些 Markdown 支持：

```md
==高亮文字==
```

更稳妥的是 HTML：

```html
<mark>高亮文字</mark>
```

混写：

```md
请注意：<mark>这里是重点</mark>
```

---

## 16）下标和上标

```md
H<sub>2</sub>O
x<sup>2</sup>
```

```html
H<sub>2</sub>O
x<sup>2</sup>
```

---

## 17）居中文本

Markdown 原生不支持居中，常用 HTML：

```html
<p align="center">这是一段居中文本</p>
```

混写：

```md
<p align="center">标题说明文字</p>
```

---

## 18）右对齐文本

```html
<p align="right">这是一段右对齐文本</p>
```

---

## 19）折叠内容

这个很常用，尤其适合 README：

```html
<details>
  <summary>点击展开</summary>

  这里是折叠后的内容。

  - 支持列表
  - 支持段落
  - 支持代码块

</details>
```

混写示例：

````md
<details>
  <summary>查看安装步骤</summary>

  ```bash
  npm install
  npm run dev
````

</details>
```

---

## 20）自定义提示块

Markdown 没有统一标准提示框，可以用 HTML 模拟：

```html
<div style="padding: 12px; border-left: 4px solid #409eff; background: #f4f8ff;">
  提示：这是一个信息提示框
</div>
```

警告框：

```html
<div style="padding: 12px; border-left: 4px solid #e6a23c; background: #fff7e6;">
  注意：这是一个警告提示框
</div>
```

错误框：

```html
<div style="padding: 12px; border-left: 4px solid #f56c6c; background: #fff1f0;">
  错误：这是一个错误提示框
</div>
```

---

## 21）插入按钮样式链接

```html
<a href="https://example.com" style="display:inline-block;padding:8px 14px;background:#1677ff;color:#fff;text-decoration:none;border-radius:6px;">
  点击查看
</a>
```

注意：有些 Markdown 平台会过滤 style。

---

## 22）图片加标题

```html
<p align="center">
  <img src="https://example.com/demo.png" alt="demo" width="500"><br>
  <em>图 1：系统演示图</em>
</p>
```

---

## 23）并排图片

```html
<p>
  <img src="https://example.com/a.png" alt="a" width="45%">
  <img src="https://example.com/b.png" alt="b" width="45%">
</p>
```

---

## 24）并排内容块

```html
<table>
  <tr>
    <td width="50%">
      左侧内容
    </td>
    <td width="50%">
      右侧内容
    </td>
  </tr>
</table>
```

Markdown 里常用这个替代复杂布局。

---

## 25）定义列表

Markdown 标准一般不支持，HTML 可以：

```html
<dl>
  <dt>HTML</dt>
  <dd>超文本标记语言</dd>

  <dt>Markdown</dt>
  <dd>轻量级标记语言</dd>
</dl>
```

---

## 26）锚点跳转

### 目录跳转

```md
- [跳到安装](#安装)
- [跳到使用方法](#使用方法)

## 安装

这里是安装说明

## 使用方法

这里是使用说明
```

### HTML 锚点

```html
<a href="#part1">跳到第一部分</a>

<h2 id="part1">第一部分</h2>
```

---

## 27）插入原始 HTML 区块

```md
<div>
  <h3>这是 HTML 区块标题</h3>
  <p>这是 HTML 区块内容</p>
</div>
```

---

## 28）转义 HTML 字符

当你想展示标签本身而不是让它生效时：

```html
&lt;div&gt;这不是实际标签，而是展示出来的文本&lt;/div&gt;
```

常见实体：

```txt
<  -> &lt;
>  -> &gt;
&  -> &amp;
"  -> &quot;
```

---

# 混写完整模板示例

## 29）README 顶部模板

````md
<h1 align="center">项目名称</h1>

<p align="center">
  项目简介一句话说明
</p>

<p align="center">
  <a href="#功能">功能</a> |
  <a href="#安装">安装</a> |
  <a href="#使用">使用</a> |
  <a href="#截图">截图</a>
</p>

---

## 功能

- [x] 支持登录
- [x] 支持数据展示
- [ ] 支持导出

## 安装

```bash
npm install
npm run dev
````

## 使用

请访问：`http://localhost:3000`

## 截图

<p align="center">
  <img src="https://example.com/screenshot.png" alt="截图" width="700">
</p>
```

---

## 30）带折叠说明的 FAQ 模板

````md
## FAQ

<details>
  <summary>1. 如何安装？</summary>

  使用以下命令：

  ```bash
  npm install
````

</details>

<details>
  <summary>2. 如何启动？</summary>

使用以下命令：

```bash
npm run dev
```

</details>
```

---

## 31）图文说明块模板

```md
## 功能演示

<p align="center">
  <img src="https://example.com/demo.png" alt="demo" width="600">
</p>

<p align="center">
  <em>图：功能演示界面</em>
</p>

说明：

- 左侧是导航菜单
- 中间是内容区域
- 右上角是操作入口
```

---

## 32）提示说明块模板

```md
<div style="padding: 12px; border-left: 4px solid #67c23a; background: #f0f9eb;">
  成功：配置已完成
</div>

<div style="padding: 12px; border-left: 4px solid #e6a23c; background: #fdf6ec;">
  注意：某些平台会过滤 HTML 样式
</div>

<div style="padding: 12px; border-left: 4px solid #f56c6c; background: #fef0f0;">
  错误：请检查配置文件路径
</div>
```

---

# 平台兼容性提醒

不是所有 Markdown 渲染器都完全支持 HTML 混写，常见情况如下：

## 一般支持较好

* GitHub README
* GitLab
* Typora
* 部分静态博客系统

## 可能有限制

* 有些平台会过滤：

  * `<style>`
  * `<script>`
  * `iframe`
  * 内联 `style`
  * 某些表单元素

所以经验上：

* **内容结构** 用 Markdown
* **对齐、颜色、折叠、布局** 用少量 HTML
* **复杂样式** 不要过度依赖 HTML

---

# 最实用速查小抄

````md
# 标题
## 二级标题

**加粗**
*斜体*
~~删除线~~

> 引用内容

- 无序列表
1. 有序列表

[链接文字](https://example.com)
![图片说明](https://example.com/a.png)

`行内代码`

```js
console.log("hello");
````

---

| 列1 | 列2 |
| -- | -- |
| A  | B  |

<span style="color:red;">红字</span>

<mark>高亮</mark>

H<sub>2</sub>O
x<sup>2</sup>

<p align="center">居中文本</p>

<p align="center">
  <img src="https://example.com/a.png" width="300" alt="示例图">
</p>

<details>
  <summary>点击展开</summary>

这里是折叠内容

</details>
```