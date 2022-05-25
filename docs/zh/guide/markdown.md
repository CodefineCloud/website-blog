## 链接
<!-- 相对路径 -->
[首页](../README.md)  
[配置参考](../reference/config.md)  
[快速上手](./getting-started.md)  
<!-- 绝对路径 -->
[指南](/zh/guide/README.md)  
[配置参考 > markdown.links](/zh/reference/config.md#links)  
<!-- URL -->
[GitHub](https://github.com) 

## Emoji
VuePress 2 已经发布 :tada: ！

## 目录
[[toc]]

## 代码块
```ts{1,6-8}
import { defaultTheme, defineUserConfig } from 'vuepress'

export default defineUserConfig({
  title: '你好， VuePress',

  theme: defaultTheme({
    logo: 'https://vuejs.org/images/logo.png',
  }),
})
```

### 禁用行号
```ts
// 行号默认是启用的
const line2 = 'This is line 2'
const line3 = 'This is line 3'
```

```ts:no-line-numbers
// 行号被禁用
const line2 = 'This is line 2'
const line3 = 'This is line 3'
```

### v-pre
```md
<!-- 默认情况下，这里会被保持原样 -->
1 + 2 + 3 = {{ 1 + 2 + 3 }}
```

```md:no-v-pre
<!-- 这里会被 Vue 编译 -->
1 + 2 + 3 = {{ 1 + 2 + 3 }}
```

```js:no-v-pre
// 由于 JS 代码高亮，这里不会被正确编译
const onePlusTwoPlusThree = {{ 1 + 2 + 3 }}
```

### 导入代码块
不支持热更新
<!-- 最简单的语法 -->
@[code](../foo.js)

<!-- 仅导入第 1 行至第 10 行 -->
@[code{1-10}](../foo.js)

<!-- 指定代码语言 -->
@[code ts](../foo.js)

<!-- 行高亮 -->
@[code js{2,4-5}](../foo.js)

@[code{3-10} js{3}:no-line-numbers](../foo.js)

## 使用Vue
一加一等于： {{ 1 + 1 }}

<span v-for="i in 3"> span: {{ i }} </span>

### 组件
这是默认主题内置的 `<Badge />` 组件 <Badge text="演示" />

## 静态资源

### 图片
![图片](./avatar.jpg)

![VuePress Logo](/images/pub.jpeg)