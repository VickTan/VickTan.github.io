# Frontend Mentor - Social links profile solution

This is a solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

### Links

- Solution URL: [[GitHub - VickTan/VickTan.github.io: Social links profile](https://github.com/VickTan/VickTan.github.io)]
- Live Site URL: https://vicktan.github.io/

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

#### 1. 通过伪类选择处于特殊状态的选择器，并设置其状态。

伪类是选择器的一种，用于选择处于特殊状态的元素。通过伪类即可为元素设置特殊状态下的样式。一般上:伪类就是开头为冒号的关键字。例如，:hover就是一个伪类

伪类可以分为以下两种：

- 简单伪类
  
  - `:last-child`
  
  - `:first-child`
  
  - `:only-child`
  
  - 等等

- 用户行为伪类
  
  一些伪类只适用于用户以某种方式与文档交互时。
  
  例如，
  
  - `:hover`
  
  - `:focus`
  
  - 等等

本次练习中，悬浮状态的样式就需要用到伪类来设置。

```css
.list-item:hover{
    background-color: hsl(75, 94%, 57%);
    color: black;
    cursor: pointer;
    
}
```

上方代码表示,类名为list-item的元素在用户将光标移到其上方时，背景颜色会改变成`hsl(75, 94%, 57%L)` ；字体颜色变成黑色，光标呈现为指示链接的指针（一只手）



#### 语义化HTML

语义化HTML是指通过选择具有明确含义的HTML标签来描述网页内容的结构和意义，而不仅仅是将其是为布局的容器。它的核心思想是让代码既能被浏览器正确渲染，又能被开发者、辅助工具（如屏幕阅读器）和搜索引擎“读懂”。

语义化HTML，顾名思义标签的名称明确指示了内容的一样。提高代码的可维护性、便于辅助工具读取有用信息。

常见的语义化HTML,如下：

- <main>  ：表示网页中的关键内容

- <header> ： 为文档或节指定页面。一般用作介绍性内容的容器
  
  - 既可以表示整个网页的头部，也可以表示一篇文章或者一个区块的头部
  
  - 

- <footer> ：为文档或节规定页脚
  
  - 页脚通常包含文档的作者、版权信息、使用条框链接、联系信息等
  
  - 

-  <nav>  ：定义导航链接集合。
  
  - <nav> 标签通常放置在<header>里面，不适合放在<footer>
  
  - <nav>标签通常时列表，也可以放置其他标签

- <section> ： 定义文档中的节
  
  - 可以将网站首页划分为简介、内容、联系信息等节
  
  - <section>标签内应该包含<h1>~<h6>标签

- <article> ：规定独立的自包含内容
  
  - 文档有其自身的意义，并且可以独立于网站其他内容进行阅读
  
  - 应用场景
    
    - 论坛
    
    - 博客
    
    - 新闻

- <aside> : 页面主内容之外的某些内容（比如侧边栏）
  
  - <aside>内容应该与周围内容相关
  
  - 用来表示与网页或者文章主要内容相关，但不属于主要内容的部分
  
  - 通常用于表示侧边栏、推荐文章、广告、相关链接等信息
  
  - 在文章级别中<aside>可以用来放置文章的补充信息、评论或注释等信息

- ........

结合语义化HTML,HTML大概结构可以按照下方图片设计：

![](C:\Users\11857\AppData\Roaming\marktext\images\2025-03-17-16-27-46-image.png)

本次应用：

```html
<body>

  
  <main class="pageMain">
    <div class="root">
      <!-- <header></header>
      <nav></nav> -->
      <div class="socialLinkProfileCard">
        <section class="profileSection">
          <div class="profile">
            <img class="profile-avatar" alt="avatar jessica" src="./assets/images/avatar-jessica.jpeg" >
            <div class="profile-person">
              <p class="profile-name">Jessica Randall</p>
              <p class="profile-address">London, United Kingdom</p>
            </div>
            <p class="profile-introduction">"Front-end developer and avid reader."</p>
          </div>
        </section>
        <section class="socialLink">
          <div class="list">
            <div class="list-item">GitHub</div>
            <div class="list-item">Frontend Mentor</div>
            <div class="list-item">LinkedIn</div>
            <div class="list-item">Twitter</div>
            <div class="list-item">Instagram</div>
          </div>
        </section>
        
      </div>
      <!-- <footer>
        <div class="attribution">
          Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
          Coded by <a href="#">yoyo Tan</a>
        </div>
      </footer> -->
    </div>
    
  </main>
  
  
</body>
```



#### Figma上一些内容的含义

- spacing/200：是设计系统中对间距的统一命名，用于规范元素之间的间距。
  
  - /200：表示间距的等级（或比例），数字越大，间距越大。例如：
    
    - `spacing/50` → 4px
    
    - `spacing/100` → 8px
    
    - `spacing/200` → 16px
    
    - `spacing/300` → 24px
    
    -  **（具体数值因设计系统而异）**

- Width、Height的相关属性
  
  - Fill：填充父容器的剩余空间（宽度或高度占满可用区域）
    
    - 使用场景：背景、响应式布局中的自适应区块
      
      - CSS实现：
        
        - 块级元素默认行为：宽度占满父容器（需父容器有明确宽度）
        
        - 动态填充剩余空间：使用Flexbox或Grid布局
          
          - 通过Flexbox实现
            
            ```css
            /* Flexbox 实现 */
            .parent {
              display: flex;
            }
            .element-fill {
              flex: 1; /* 占满剩余空间 */
            }
            ```
          
          - 通过Grid布局实现
            
            ```css
            /* Grid 实现 */
            .parent {
              display: grid;
              grid-template-columns: 200px 1fr; /* 1fr 表示填充剩余空间 */
            }
            .element-fill {
              grid-column: 2;
            }
            ```
          
          - 传统百分比（需父容器有明确尺寸）
            
            ```css
            /* 传统百分比（需父容器有明确尺寸） */
            .element-fill {
              width: 100%;
              height: 100%;
            }
            ```
        
        
  
  - Fixed：固定模式，表示元素的宽度或高度不会根据内容或父容器自动调整，而是保持指定的固定值
    
    - 使用场景：图标、固定宽高的按钮、分割线
  
  - Hug：尺寸自动适应内容（如文本长度、子元素大小
    
    - 使用场景：标签、动态按钮
    
    - CSS中的实现
      
      - 将属性值指定为：max-content 
        
        ```css
        .element-hug {
          width: max-content;   /* 宽度由内容决定 */
          display: inline-block; /* 或 inline-flex/inline-grid */
        }
        ```
        
      
      - 使用Flexbox
        
        ```css
        /* 或使用 Flexbox */
        .parent {
          display: flex;
        }
        .element-hug {
          flex: none; /* 禁止拉伸，宽度由内容决定 */
        }
        ```
        
        
        
        



### Continued development

- 语义化HTML

- 伪类和伪元素

- Figma一些专业性用语

### Useful resources

- [HTML5 语义元素](https://www.w3school.com.cn/html/html5_semantic_elements.asp)- 该文章让我大概了解HTML语义
- [[方向三：前端实践-HTML语义化的案例分析 | 豆包MarsCode AI刷题一、HTML语义化和非语义化 （1）HTM - 掘金](https://juejin.cn/post/7441944462933721125)](https://blog.csdn.net/m0_61505785/article/details/145660750)- 该文章让我知道为什么要用语义化HTML
