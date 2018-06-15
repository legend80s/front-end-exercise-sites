# front-end-exercise-sites
> 优秀前端工程师的进化之路，知识点全覆盖。
>
> 目标是从入门级别前端工程师脱胎换骨为独当一面的职业前端工程师。

秉着以兴趣为导向的宗旨，若不感兴趣的知识点可先略过，注重把功能完成，以后回过头来再仔细研究遗漏的知识点。

## 需求

从简单需求出发。实现类似优酷的搜索下拉提示效果，具体要求：

1. 输入文字展现相应下拉提示结果
2. 高亮匹配的查询词
3. 点击下拉提示结果自动替换到输入框（优酷的效果是点击后直接搜索）
4. 前三条下拉提示序号标红凸显为热词
5. 点击搜索“🔍”图标搜索查询词
6. 初始化时即未输入任何字符显示十条热搜

## 进化之路

完成基本需求后开始进化。

### 目标

独当一面的职业前端工程师

### 做一个“有礼貌”的前端

“做事先做人”，先从基本礼仪开始，做一个“有礼貌”的前端，大家才能喜欢你。可先跳过，但该规范部分必须始终贯穿你的编码生涯。

- CSS 须符合 [CSS 编码规约](https://github.com/legend80s/front-end-exercise-sites/blob/master/code-style-guide/css.md)
- HTML 须符合 [HTML 编码规约](https://github.com/legend80s/front-end-exercise-sites/blob/master/code-style-guide/html.md)
- JavaScript 须符合 Airbnb 代码规范 [英文版](https://github.com/airbnb/JavaScript)，英语差的同学看 [中文版](https://github.com/yuche/javascript) 👎
- 文字排版须符合 [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)
- Git 提交信息须须合 [Git 提交信息规范](https://mp.weixin.qq.com/s/WwTQVGm5WjFXJc0JBlytMw)
- 好的命名是艺术。参见《代码大全》变量名的力量 The Power of Variable Names

### 基础进化

洪荒时代，一切都得刀耕火种，虽然辛苦，但自己一笔一划打下的基础最牢固！

调试技巧之打断点 https://www.zhihu.com/question/43687153 将会伴随你的前端生涯。

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
      * @return {void}
      *
      * @example
      * jsonp('http://tip.soku.com/search_tip_1', {
      *   queryKey: 'query',
      *   queryValue: '北京',
      *   callbackKey: 'jsoncallback',
      * }, function handleResponse(response) {
      *   console.log('response:', response);
      * })
     ```

5. [Feature] jsonp 增加错误处理，加入错误提示展现给用户。学会经典的 callback 错误处理机制。

   - 重要性：为以后学习和比较 Promise 的 catch 做准备。

   - 函数签名一样，只是 callback 形参不一样。用法如下

     ```javascript
     jsonp('http://tip.soku.com/search_tip_1', {
       queryKey: 'query',
       queryValue: '北京',
       callbackKey: 'jsoncallback',
     }, function handleResponse(error, response) {
       if (error) {
         console.error('error:', error);
         return;
       }
     
       console.log('response:', response);
     });
     ```

6. [Refactor] 封装为类，用 prototype 的方式。了解四五种继承方案，各自优劣点，自己 pick 一种，为什么选择该种？

7. [Feature] 增加腾讯视频下拉提示，左侧增加可选的下拉

   ![searcher](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/searcher.png)

8. [Feature] 增加三块区域，tab 切换

   - 网址大全。静态的网址

   - 视频。API 摘取自 360 导航

      API `http://open.onebox.so.com/dataApi?&tpl=2&callback=legend.cb.get360RankedVideos&_1528902170281&query=%E7%BB%BC%E8%89%BA&url=%E7%BB%BC%E8%89%BA%E6%8E%92%E8%A1%8C&type=relation_variety_rank&src=onebox&num=1&addInfo=types:%E5%85%A8%E9%83%A8|region:%E5%85%A8%E9%83%A8|year:%E5%85%A8%E9%83%A8|limit:10|page:1`

   - 新闻。API 摘取自 360 导航

      API `https://pc.api.btime.com/btimeweb/getInfoFlow?callback=jQuery111308214331648120714_1528901698870&channel=news&request_pos=channel&citycode=local_330500_330000&sub_channel=&refresh=6&req_count=6&refresh_type=2&pid=3&from=&page_refresh_id=bdd83c10-6f19-11e8-8796-6c92bf0a9cdb&_=1528901698882`

   - 效果图：配色不要求一模一样，用自己喜欢的即可

      - 网址：

      ![favorite-sites](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/favorite-sites.png)

      - 视频

      ![videos](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/videos.png)

      - 新闻

      ![news](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/news.png)

9. [Refactor] 组件化。相同的重复的模块，封装为组件。比如某个视频和某条新闻都有相似的结构和功能

   - 重要性：为提倡“组件化优先”的框架学习打基础
   - 重要性：DRY 原则

10. [Feature] 记住用户的搜索历史。显示给用户。分别用 cookie 和 localStorage 实现

11. [Refactor Performance] `createDocumentFragment` 重构渲染函数。并深入了解该方法的好处

### 中级进化

#### 目标

成为一个合格的职场前端

#### 进化为 ES5

进入摩登时代，首先要做一个遵纪守法的人，所谓“仓廪实而知礼节”，基础打好了，人品也要跟得上

1. [Doc] 使用 jsdoc 注释你的每一个函数，DocBlockr 会帮你的。
   - 注释将帮助养成你先想后写的好习惯。一般函数名、形参、返回值固定则函数架构基本已完成
   - 如果函数描述过长，则应该反思是否违反了 Single Responsibility 原则
   - 好的注释对未来的你和你的合作者都是一笔财富
2. [Refactor] for 循环用 forEach 替换。并了解数组的
   - 处理方法：map reduce filter splice slice
   - 查找方法：find includes indexOf some every
3. [Performance] 防止输入频繁导致发送不必要请求，写 debounce 函数。
   - 重要性：函数式编程之高阶函数

4. TODO

#### 进化为 ES6

进入后现代，体会 JS 的小巧与精致，做一个精致的前端男孩

1. [Refactor] 字符串拼接改为模板字符串的插值方式 
2. 函数默认值
3. [Refactor] 对象属性简写
4. [Refactor] 用 const let 替换 var
5. [Refactor] 用箭头函数替换普通行数，并了解其好处。**arrow function will save you from the nightmare of wtf-is-this**。
6. 函数参数用参数解构（parameter destructuring）改写
7. [Refactor] 重构为 es6 class。并了解继承
8. [Refactor] jsonp 改为 Promise 形式。用 then 调用。
   1. 和 callback 比较，为什么说 Promise saves you from the callback hell？
   2. 熟悉 Promise 的实例方法 catch finally 和静态方法 all race
9. [Refactor] Promise 的调用改为 aync / await。并体会其好处。

### 高级进化

#### 目标

成为一个可独当一面的职场前端。主要在发力在打包构建、框架、新思想新语言方面

1. Webpack 3，结合 babel-loader 让我们有能力用未来的技术编程 

   - *TODO*

   - less sass。至少会一种
   - 熟悉所有 es6 语法；知道 es7 的新特性 

2. 函数式编程
   - js 哪些方法支持函数式编程
   - 用函数式编程重构

3. 新建一个项目，用 Vue.js 重构下拉提示

4. 新建一个项目，用 typescript 重构

5. 增加单测（可选）

### 超脱进化

不做要求

#### 目标

Hold 住后端。剑指后端 Node.js

*TODO*

### Revolution to be continued...

若所有任务均完成，还有以下知识点不知道，请继续深造

1. 伪类伪元素，及其区别
2. 原型链
3. 闭包
4. fetch
5. canvas 绘图
6. 安全 CSRF XSS
7. CORS
8. YSlow 35 rules - http://checkmyws.github.io/yslow-rules/
9. Restful API
10. 编程范式
11. 设计模式

## 博客和网站推荐

1. [阮一峰的个人网站](http://www.ruanyifeng.com/home.html) 和他的微信公众号【阮一峰的网络日志】
2. CSS 属性不会用看这个网站 <https://cssreference.io/> 

