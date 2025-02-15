# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

![](C:\Users\11857\AppData\Roaming\marktext\images\2025-02-16-00-06-49-image.png)<img title="" src="file:///C:/Users/11857/AppData/Roaming/marktext/images/2025-02-16-00-07-18-image.png" alt="" data-align="inline">

### Links

- Solution URL: [GitHub - VickTan/VickTan.github.io: Blog preview card solution](https://github.com/VickTan/VickTan.github.io)
- Live Site URL: https://vicktan.github.io/

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- 学会如何引入自定义字体
  
  `@font-face` CSS at-rule 指定一个用于显示文本的自定义字体；字体能从**远程服务器**或者**用户本地安装的字体**加载。
  
  @font-face 可以消除对用户电脑字体的依赖。 
  
  引入本地字体的步骤如下：
  
  - 准备字体：
    
    可以从多种平台获取外部字体，如Google Fonts、Adobe Fonts等。将字体下载到本地。
    
    常见的字体格式有：
    
    - .ttf：TrueType字体
    
    - .otf：OpenType字体
    
    - .woff、.woff2：Web优化字体格式
    
    不同的浏览器支持的字体格式有所不同
  
  - 使用@font-face引入字体
  
  ```css
  @font-face {
      font-family: 'Figtree';
      src: url('./assets/fonts/static/Figtree-ExtraBold.ttf') format('truetype');
      font-weight: 800;
      font-style: normal;
      font-display: swap;
  }
  
  @font-face {
      font-family: 'Figtree';
      src: url('./assets/fonts/static/Figtree-SemiBold.ttf') format('truetype');
      font-weight: 600;
      font-style: normal;
      font-display: swap;
  }
  
  @font-face {
      font-family: 'Figtree';
      src: url('./assets/fonts/Figtree-Italic-VariableFont_wght.ttf') format('truetype');
      font-weight: 100 900;
      font-style: italic;
      font-display: swap;
  }
  
  @font-face {
      font-family: 'Figtree';
      src: url('./assets/fonts/Figtree-VariableFont_wght.ttf') format('truetype');
      font-weight: 100 900;
      font-style: normal;
      font-display: swap;
  }
  ```

- 学会如何通过media，来进行媒体查询的响应式
  
  ```css
  /* 屏幕宽度大于 600px 且支持悬停操作的设备 */
  @media screen and (min-width: 600px) and (hover: hover) {
    body { background: lightblue; }
  }
  
  /* 打印或屏幕宽度小于 400px 的设备 */
  @media print, (max-width: 400px) {
    body { font-size: 12pt; }
  }
  
  /* 仅适用于不支持脚本的设备 */
  @media not script {
    .noscript-warning { display: block; }
  }
  ```

- 通过gap属性设置网格（grid）和弹性盒子（Flexbox）布局中子元素之间的间距属性
  
  基本语法：
  
  ```css
  gap: <row-gap> <column-gap>;
  ```
  
  ```css
  .attribution { 
      display: flex;
      flex-direction: column;
      gap: 24px;
      width: 279px;
      height: 453px;
      background-color: white;
      padding: 24px;
      border-radius: 20px;
  }
  ```

- 

### Continued development

- Boostrap

- 响应式设计

### Useful resources

- [@font-face - CSS：层叠样式表 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@font-face) 
- 
