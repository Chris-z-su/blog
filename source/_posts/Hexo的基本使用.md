---
title: Hexo的基本使用
excerpt: Hexo命令的基本使用，常用配置以及代码提交等。
date: 2022-05-02 07:40:25
tags:
---
> https://hexo.io/zh-cn/docs/commands
## 1. 初始化项目
```
$ hexo init [folder]
```
## 2. 新建文件
```
$ hexo new [layout] <title>
```
> https://hexo.io/zh-cn/docs/templates

可选参数（layout）如下：
| 模板     | 用途     | 回退    |
| -------- | -------- | ------- |
| index    | 首页     |         |
| post     | 文章     | index   |
| page     | 分页     | index   |
| archive  | 归档     | index   |
| category | 分类归档 | archive |
| tag      | 标签归档 | archive |

```
$ hexo new "post title with whitespace"
```

## 3. 文章内容详解
```
title: Hexo的基本使用  # 文章标题
index_img: /img/3.jpg  # 首页图片
banner_img: /img/3.jpg  # 文章页面图片
date: 2022-05-02 07:40:25  # 文章发布时间
tags:  # 文章标签
```

## 4. 项目提交发布
> 参考：https://hexo.io/zh-cn/docs/github-pages
> https://blog.csdn.net/sinat_37781304/article/details/82729029

### 1) hexo clean清除了你之前生成的东西，也可以不加。
```
hexo clean
```

### 2) hexo generate 顾名思义，生成静态文章，可以用 hexo g缩写
```
hexo generate
```

### 3) hexo deploy 部署文章，可以用hexo d缩写
```
hexo deploy
```

## 5. Hexo fluid主题更新
> https://hexo.fluid-dev.com/docs/start/#%E6%9B%B4%E6%96%B0%E4%B8%BB%E9%A2%98



## 99. 其他
### ① hexo d命令报错：ERROR Deployer not found: git
参考：
> https://developer.aliyun.com/article/764974
解决
安装hexo-deployer-git：
```
npm install --save hexo-deployer-git
```


