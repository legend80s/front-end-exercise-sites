*待整理*

## 问题

1. 为什么 input 需要增加 input 和 click 事件？

2. target 和 currentTarget 有何区别？

3. 为什么要封装一个最底层的 jsonp 函数，和 youkuJsonp？

4. 以下代码什么意思？比如输入什么，输出什么？

   ```javascript
   return response.r.map(function (item) {
     return item.w;
   });
   ```

5. 采用 innerText == '' 的形式情况下拉提示，假如不使用事件委托会有什么问题？

## 答案

第二点关键在如何实现高亮函数，满足以下测试用例

```javascript
highlight('北京', '北京女子图鉴') === '<b>北京</b>女子图鉴'
highlight('北京', '北京女子图鉴', 'i') === '<i>北京</i>女子图鉴'
highlight('女子', '北京女子图鉴') === '北京<b>女子</b>图鉴'
```

答案：
函数注释，请安装 DocBlockr

```javascript
/**
 * 高亮匹配关键词
 * 
 * @param  {string} query      关键词
 * @param  {string} suggestion 下拉提示结果
 * @param  {string} [tagName=b] 高亮元素
 * 
 * @return {string}            高亮后的下拉提示
 *
 * @example
 * highlight('北京', '北京女子图鉴')
 * // => <b>北京</b>女子图鉴
 *
 * highlight('北京', '北京女子图鉴', 'i')
 * // => <i>北京</i>女子图鉴
 *
 * highlight('女子', '北京女子图鉴')
 * // => 北京<b>女子</b>图鉴
 */
function highlight(query, suggestion, tagName = 'b') {
  return suggestion.replace(query, matchedQuery => `<${tagName}>${matchedQuery}</${tagName}>`);
}

// 说明
// `<${tagName}>${matchedQuery}</${tagName}>`
// 等价于
// '<' + tagName + '>' + matchedQuery + '</' + tagName + '>'
// 显然 string interpolation 的方式更剪短更易读
```
