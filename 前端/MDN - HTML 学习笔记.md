# MDN - HTML 学习笔记

## 基础语法

### 什么是 HTML

HTML（HyperText Markup Language，**超文本标记语言**），是一种**标记语言**。

> [!TIP]
>
> - 尽可能只使用 `index.html` 文件。
> - 所有标签都用小写书写。

> [!NOTE]
>
> - **元素**（Element）是**开始标签**（Opening tag）、**内容**（Content）和**结束标签**（Closing tag）的总和。
>
> ![grumpy-cat-small](.\MDN - HTML 学习笔记.assets\grumpy-cat-small.png)

### 空元素及自闭合标签

**空元素**（void element）是 HTML 中不能存在**子节点**的元素。

> [!NOTE]
>
> - HTML 中不存在**自闭和标签**（`<tag />`），但也是一种有效的语法。
>
> - 自闭合标签是为了兼容 **XHTML** 和更易读。

### 布尔属性

没有值的属性。当出现时，其值被设置为 `true`，否则默认为 `false`。

### 属性值引号

> [!TIP]
>
> - 只使用**双引号**。
> - 当属性值中出现双引号时，使用**字符引用**（`&quot;`）。

## 文本格式化

### 标题和段落

### div 标签

> [!TIP]
>
> `div`：“div”是“division”（分隔）的缩写
>
> 

### 列表

#### 无序列表

`ul`、`li`。

- `ul`：（**Unordered List**，无序列表）；

- `li`：（**List Item**，列表项）；

#### 有序列表

`ol`、`li`。

- `ol`：（**Ordered List**，有序列表）；

- `li`：（**List Item**，列表项）；

#### 定义列表

`dl`、`dt`、`dd`。

- `dl`：（**Definition List**，定义列表）；

- `dt`：（**Definition Term**，定义术语）；

- `dd`：（**Definition Description**，定义描述）。

> [!WARNING]
>
> - 像`<b>`、`<i>` 和 `<u>` 这样，仅仅影响表象而没有语义的元素，被称为**表现元素**（presentational element）。
> - 尽可能使用**语义元素**，避免使用**表现元素**。

### 

## 基本页面结构

- **页眉**（`<header>`）
- **导航栏**（`<nav>`）
- **主内容**（`<main>`）
- **侧边栏**（`<aside>`），经常放置在 `<main>` 中。
- **页脚**（`<footer>`）

![sample-website](.\MDN - HTML 学习笔记.assets\sample-website.png)

## 超链接

超链接 `a`（**anchor**，意为**锚点**）。

#### 属性

- `href`，是 **hypertext reference**（超文本引用） 的缩写。

- `title`，悬停时的提示。

- `target`，在**哪里**打开此链接。

  - `_self`（**默认值**）：在当前标签页打开（覆盖当前页面）；
  - `_blank`：在新标签页打开；

- `rel`，是 **Relationship** 的缩写，用来描述**目标资源**与**当前页面**的**关系**。

  - `nofollow`：不给搜索引擎传递权重。

  - ## `sponsored`：表示指向

#### 页面锚点

- `href = "#[id]"   id="..."`；
- `<a name="...">`

自带锚点：`#top`；

#### 下载

- 普通下载：（直接通过 `href` 属性指向要下载的文件）
  ```html
  <a href="./HTML.zip">...</a>
  ```

- 强制下载（通过 `download` 属性强制下载）
  ```html
  <a href="./HTML.pdf" download>...</a>
  ```

  - 通过 `download` 属性值来指定下载文件名：
    ```html
    <a href="./HTML.png" download="HTML 示例图片">...</a>
    ```

#### 邮件链接

`mailto`（**mail** to）+`:[...]`（邮箱地址）。

```html
<a href="mailto:example@qq.com">...</a>
```

#### 电话链接

`tel` + `:[...]`（电话号码）。

```html
<a href="tel:18112345678">...</a>
```



## 图片

> [!TIP]
>
> **图像四要素**：
>
> - `src`
> - `alt`
> - `width`
> - `height`

#### 相对路径和绝对路径



## 视频和音频

### 音频

`audio`：



## 表格

## 表单和按钮

## 调试

## 其他



