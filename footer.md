#css五种方式实现footer置底
页脚置底（Sticky footer）就是让网页的footer部分始终在浏览器窗口的底部。

当网页内容足够长以至超出浏览器可视高度时，页脚会随着内容被推到网页底部；但如果网页内容不够长，置底的页脚就会保持在浏览器窗口底部。

##1. 将内容部分的底部外边距设为负数 
这是个比较主流的用法，把内容部分最小高度设为100%，再利用内容部分的负底部外边距值来达到当高度不满时，页脚保持在窗口底部，当高度超出则随之推出的效果。
`<body>`
  `<div class="wrapper">`
  
      `content`
      
   ` <div class="push"></div>`
  `</div>`
  `<footer class="footer"></footer>`
`</body>`
`html, body {`
  `height: 100%;`
 ` margin: 0;`
`}`
`.wrapper {`
  `min-height: 100%;`

  `/* 等于footer的高度 */`
 ` margin-bottom: -50px;`
`}`
`.footer,`
`.push {`
 ` height: 50px;`
`}`
这个方法需要容器里有额外的占位元素（如.push）
需要注意的是.wrapper的margin-bottom值需要和.footer的负的height值保持一致，这一点不太友好。
