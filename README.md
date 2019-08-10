# Road to Frontend Engineer

> 前端工程师的进化之路，知识点全覆盖。
> 目标是从入门级别前端工程师脱胎换骨为独当一面的职业前端工程师。

秉着以兴趣为导向的宗旨，若不感兴趣的知识点可先略过，注重把功能完成，以后回过头来再仔细研究遗漏的知识点。

## Tasks
1. React 或 Vue 写个项目。项目可从兴趣或实用出发，日常用到但不方便，比如逛的网站很多，放在 bookmarks 不方便，那不妨写一个网址导航；模仿图片网站 <https://www.pexels.com/>，训练自己的 CSS 布局能力；豆瓣租房人工刷选工作量大，写个爬虫，数据通过页面展示出来……。目标是能自信的说自己能独立搭建项目
2. lodash：若无，引入该常用 util 方法库。目标：熟悉安装依赖流程、体会引入外包依赖的重要性
2. ESlint：若无，给项目加 eslint。目标是熟悉 Airbnb JavaScript 和 React 规范
3. jsdoc：安装 DocBlockr 给方法或函数加注释。目标提升代码可读性
4. 组件化：大块代码切分为小的组件。目标了解组件化思维，一切皆组件。
5. React Hooks：若无，给项目加 hooks。目标是熟练使用 React 新技术
6. UT：若无，给项目的所有 util 方法加单测。目标是抓代码质量
7. TypeScript：项目 ts 化。目标是熟悉现代前端工程师必备新技能之一
8. Node.js：react / vue 项目调用自己写的接口。目标是熟悉现代前端工程师必备技能之一
9. Restful API：让接口符合 rest 规范。目标了解 rest：HTTP method 和 status code - https://http.cat/
10. FP：学习 JavaScript 函数式编程（Functional Programming），吸取其精华应用到项目中
11. SOLID：学习面向对象 SOLID 原则，并应用到项目中
12. 算法基础：《剑指 offer》。目标是了解，无需深入否则浪费时间，对其要求不高，权重因此下降

其他技巧和注意事项：

1. 禁止 for 和 for in 循环，用其他循环替代 for 循环（map reduce filter……）
2. flex 布局
2. DRY
3. KISS
4. Readability
5. CR。https://mp.weixin.qq.com/s/OCeOMmLDl6TgaJD8HuroVg

## 训练开始

从简单需求出发。实现类似优酷的搜索下拉提示效果，具体要求：

1. 输入文字展现相应下拉提示结果
2. 高亮匹配的查询词
3. 点击下拉提示结果自动替换到输入框（优酷的效果是点击后直接搜索）
4. 前三条下拉提示序号标红凸显为热词
5. 点击“搜索”按钮跳转到相应网站搜索
6. 初始化时即未输入任何字符显示十条热搜

## 进化之路

完成基本需求后开始进化。

### 目标

独当一面的职业前端工程师

### 进化之前

#### 经验

1. [调试技巧之打断点](https://www.zhihu.com/question/43687153) 将伴随你的前端生涯。

2. “腹有草稿，方能成竹在胸”。一个行之有效的开发经验是：先勾勒静态页面。即先把 HTML 结构写出来，CSS 稍修饰之，最后再加入 JavaScript 使之动态化。这样做是因为：

   - HTML 结构就像房屋结构，是基础建设。HTML 结构一出来，JS 逻辑就水到渠成，呼之欲出
   - 而且 HTML 的复杂度和 JS 的复杂度成正比，简单清晰的结构往往会导致同样简单清晰的逻辑。*BUT NO SIMPLER！*

#### 规范

“做事先做人”，先从基本礼仪开始，做一个“有礼貌”的前端，如此这般方可人见人爱。

*以下规范，现可不必逐条细读，但必须始终贯穿你的编码生涯。*

- CSS 须符合 [CSS 编码规约](https://github.com/legend80s/front-end-exercise-sites/blob/master/code-style-guide/css.md)
- HTML 须符合 [HTML 编码规约](https://github.com/legend80s/front-end-exercise-sites/blob/master/code-style-guide/html.md)
- JavaScript 须符合 Airbnb 代码规范 [英文版](https://github.com/airbnb/JavaScript)，英语差的同学看 [中文版](https://github.com/yuche/javascript) 👎
- 文字排版须符合 [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)
- Git 提交信息须须合 [Git 提交信息规范](https://mp.weixin.qq.com/s/WwTQVGm5WjFXJc0JBlytMw)
- 变量命名必须符合 [变量命名规范](https://github.com/legend80s/front-end-exercise-sites/blob/master/naming.md)

### 基础进化

洪荒时代，一切都得刀耕火种，虽然辛苦，但自己一笔一划打下的基础最牢固！

### 目标

牢固的基础，轻松面对面试官和以后繁琐的日常工作。

1. [Refactor] 数据处理和渲染隔离。体现 S.O.L.I.D 中的 Single Responsibility。“函数不能超过 80 行”的规范是其形式化的体现。

   > 修改某个函数或类的原因有且只有一个，也就是说一个函数或类只能承担一种责任

2. [Refactor] 用事件委托重构

3. [Feature] 增加样式。

   - 熟悉各种 css 选择器。以及其权重。css3 增加了哪些选择权。HTML5 增加了哪些新的标签和功能？
   - 熟悉基础颜色对应的十六进制形式，比如 #f00 代表红色，看到 #f00 想到红色，反之亦然
   - 熟悉定位
   - 熟悉框模型
   - 居中输入框和下拉提示。熟悉四五种居中方式以及适用场景。如何 flex 居中。熟悉 flex 布局和 grid 布局
   - 效果图（来自 [腾讯视频](https://v.qq.com)）：

     ![searcher](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/v-qq-com-hot-search.png)

4. [Refactor] jsonp 改写为 callback 形式，并注意避免 jsonp 带入的 script 的累积问题。

   - 重要性：面向 Promise 的重要一步

   - 函数签名如下：

     ```javascript
     /**
      * jsonp 发请求
      *
      * @public
      *
      * @param  {string} url     JSONP 对应的 API 地址
      * @param  {Object} options
      * @param  {functon} callback
      * @return 
