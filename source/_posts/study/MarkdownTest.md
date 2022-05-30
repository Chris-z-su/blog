---
title: MarkdownTest
excerpt: 练习Markdown的一些基本用法
date: 2022-02-19 09:55:39
update: 2022-05-05 19:55:00
categories: Markdown
tags:
  - Markdown
  - 技术
---

# Markdown Study

## 一、what's Markdown

## 二、How to study

<img title="Raphael Lopes" src="https://images.unsplash.com/photo-1644411990121-97f041208faf?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=Mnw5MDg0MHwwfDF8YWxsfDN8fHx8fHwyfHwxNjQ0NDk2Mjky&ixlib=rb-1.2.1&q=80&w=1080" alt="null" data-align="inline">

<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

<div>
<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
</div>

<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

```
<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```

<div>
<iframe src="//player.bilibili.com/player.html?aid=851448338&bvid=BV1aL4y137cy&cid=506463410&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

</div>

<a href="超链接地址" target="_blank">超链接名</a>

示例
<a href="https://www.jianshu.com/u/1f5ac0cf6a8b" target="_blank">简书</a>

```html
<video id="video" controls="" preload="none" poster="封面">
      <source id="mp4" src="mp4格式视频" type="video/mp4">
</videos>
```

```html
<video id="video" controls="" preload="none" poster="封面">
      <source id="webm" src="webm格式视频" type="video/webm">
</videos>
```

```html
<video id="video" controls="" preload="none" poster="封面">
      <source id="ogv" src="ogv格式视频" type="video/ogv">
</videos>
```

```html
<iframe 
src="视频或者网页路径" 
scrolling="no" 
border="0" 
frameborder="no" 
framespacing="0" 
allowfullscreen="true" 
height=600 
width=800> 
</iframe>
<!-- 相当于是子网页 -->
<!-- B站分享链接提供 -->
```

```html
![](https://gitee.com/turbo-studio/image/raw/master/image/20210215225951.gif)
```



## 二、Markdown如何生成表格


| 模板     | 用途     | 回退    |
| -------- | -------- | ------- |
| index    | 首页     |         |
| post     | 文章     | index   |
| page     | 分页     | index   |
| archive  | 归档     | index   |
| category | 分类归档 | archive |
| tag      | 标签归档 | archive |


<table>
    <tr>
        <td colspan="2">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td>整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>整数类型</td>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>整数类型</td>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>整数类型</td>
        <td>long</td>
        <td>64</td>
    </tr>
</table>

<table>
    <tr>
        <td colspan="2">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td rowspan="4">整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>long</td>
        <td>64</td>
    </tr>
</table>

<table>
    <tr>
        <td colspan="2" style="text-align: center">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td rowspan="4" style="text-align: center">整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>long</td>
        <td>64</td>
    </tr>
</table>

<table>
    <tr>
        <td colspan="2" style="align: center">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td rowspan="4" style="talign: center">整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>long</td>
        <td>64</td>
    </tr>
</table>

<table align="center">
    <tr>
        <td colspan="2">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td rowspan="4">整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>long</td>
        <td>64</td>
    </tr>
</table>



<table>
    <tr>
        <td colspan="2" style="text-align: center;vertical-align:middle;">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td rowspan="4" style="text-align: center;vertical-align:middle;">整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>long</td>
        <td>64</td>
    </tr>
</table>



### 1. 普通表格

```md
使用 |文字1|文字2|
三个或多个连字符（---）分割开表头
```

代码如下：

```
| 模板     | 用途     | 回退    |
| -------- | -------- | ------- |
| index    | 首页     |         |
| post     | 文章     | index   |
| page     | 分页     | index   |
| archive  | 归档     | index   |
| category | 分类归档 | archive |
| tag      | 标签归档 | archive |
```

| 模板     | 用途     | 回退    |
| -------- | -------- | ------- |
| index    | 首页     |         |
| post     | 文章     | index   |
| page     | 分页     | index   |
| archive  | 归档     | index   |
| category | 分类归档 | archive |
| tag      | 标签归档 | archive |


也可以直接这样写，处理效果是一样的
```
|表头1|表头2|
|---|---|
|内容1|内容2|
|内容3|内容4|
```

| 表头1 | 表头2 |
| ----- | ----- |
| 内容1 | 内容2 |
| 内容3 | 内容4 |



### 2.多行多列的表格

采用HTML的代码方式，与正常的HTML代码使用一样：

其中text-align是为了文本居中（只能左右），vertical-align是垂直居中

```html
<table>
    <tr>
        <td colspan="2" style="text-align: center;vertical-align:middle;">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td rowspan="4" style="text-align: center;vertical-align:middle;">整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>long</td>
        <td>64</td>
    </tr>
    <tr>
        <td rowspan="2" style="text-align: center;vertical-align:middle;">浮点类型</td>
        <td>float</td>
        <td>32</td>
    </tr>
    <tr>
        <td>double</td>
        <td>64</td>
    </tr>
    <tr>
        <td style="text-align: center;vertical-align:middle;">字符型</td>
        <td>char</td>
        <td>16</td>
    </tr>
    <tr>
        <td style="text-align: center;vertical-align:middle;">布尔型</td>
        <td>boolean</td>
        <td>~</td>
    </tr>
</table>
```



效果如下：

<table>
    <tr>
        <td colspan="2" style="text-align: center;vertical-align:middle;">数据类型</td>
        <td>长度(位)</td>
    </tr>
    <tr>
        <td rowspan="4" style="text-align: center;vertical-align:middle;">整数类型</td>
        <td>byte</td>
        <td>8</td>
    </tr>
    <tr>
        <td>short</td>
        <td>16</td>
    </tr>
    <tr>
        <td>int</td>
        <td>32</td>
    </tr>
    <tr>
        <td>long</td>
        <td>64</td>
    </tr>
    <tr>
        <td rowspan="2" style="text-align: center;vertical-align:middle;">浮点类型</td>
        <td>float</td>
        <td>32</td>
    </tr>
    <tr>
        <td>double</td>
        <td>64</td>
    </tr>
    <tr>
        <td style="text-align: center;vertical-align:middle;">字符型</td>
        <td>char</td>
        <td>16</td>
    </tr>
    <tr>
        <td style="text-align: center;vertical-align:middle;">布尔型</td>
        <td>boolean</td>
        <td>~</td>
    </tr>
</table>

