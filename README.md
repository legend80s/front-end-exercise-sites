# Road to Frontend Engineer

> 前端工程师的进化之路，知识点全覆盖。目标是从入门级别前端工程师脱胎换骨为独当一面的职业前端工程师。

秉着以兴趣为导向的宗旨，若不感兴趣的知识点可先略过，注重把功能完成，以后回过头来再仔细研究遗漏的知识点。

## Tasks
1. React 或 Vue 写个项目。目标是能自信的说自己能独立搭建项目。
   - 项目可从兴趣或实用出发，日常用到但不方便，比如逛的网站很多，放在 bookmarks 不方便，那不妨写一个网址导航，比如 https://tophub.today/ 或 http://www.addog.vip/；或模仿图片网站 <https://www.pexels.com/>，训练自己的 CSS 布局能力（flex）；豆瓣租房人工刷选工作量大，写个爬虫，数据通过页面展示出来……。
2. lodash：若无，引入该常用 util 方法库。目标：熟悉安装依赖流程、体会引入外包依赖的重要性
3. ESlint：若无，给项目加 eslint。目标是熟悉 Airbnb JavaScript 和 React 规范
4. jsdoc：安装 DocBlockr 给方法或函数加注释。目标提升代码可读性
5. 组件化：大块代码切分为小的组件。目标了解组件化思维，一切皆组件。
6. React Hooks：若无，给项目加 hooks。目标是熟练使用 React 新技术
7. UT：若无，给项目的所有 util 方法加单测。目标是抓代码质量
8. TypeScript：项目 ts 化。目标是熟悉现代前端工程师必备新技能之一。[《TypeScript 入门教程》](https://ts.xcatliu.com/)
9. Node.js：react / vue 项目调用自己写的接口。目标是熟悉现代前端工程师必备技能之一
10. Restful API：让接口符合 rest 规范。目标了解 rest：HTTP method 和 status code - https://http.cat/
11. FP：学习 JavaScript 函数式编程（Functional Programming），吸取其精华应用到项目中
12. SOLID：学习面向对象 SOLID 原则，并应用到项目中
13. 算法基础：《剑指 offer》。目标是了解，无需深入否则浪费时间，对其要求不高，权重因此下降

其他技巧和注意事项：

1. 禁止 for 和 for in 循环，用其他循环替代 for 循环（map reduce filter……）
2. flex 布局
3. DRY
4. KISS
5. Readability
6. CR。https://mp.weixin.qq.com/s/OCeOMmLDl6TgaJD8HuroVg

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

5. [Feature] jsonp 增加错误处理，加入错误提示展现给用户。学会经典的 Node.js callback 错误处理机制。

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

7. [Feature] 增加腾讯视频下拉提示和搜索功能，左侧增加可选的下拉

   ![searcher](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/searcher.png)

   - 考察设计原则：隔离变化与不变的部分，不变的封装为函数，变化的为其形参。须善于提取差异，捕捉不变的部分，否则你会违反 DRY 原则。

8. [Feature] 增加三块区域，tab 切换。效果图的配色不要求一模一样，用自己喜欢的即可

   - 网址大全

     ![favorite-sites](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/favorite-sites.jpeg)

   - 视频。hover 视频显示橘红色边框，*API 摘取自 360 导航*

      - API `http://open.onebox.so.com/dataApi?&tpl=2&callback=legend.cb.get360RankedVideos&_1528902170281&query=%E7%BB%BC%E8%89%BA&url=%E7%BB%BC%E8%89%BA%E6%8E%92%E8%A1%8C&type=relation_variety_rank&src=onebox&num=1&addInfo=types:%E5%85%A8%E9%83%A8|region:%E5%85%A8%E9%83%A8|year:%E5%85%A8%E9%83%A8|limit:10|page:1`
      - ![videos](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/videos-hover.png)

   - 新闻。点击未读新闻刷新当前版块，*API 摘取自 [360 导航新闻版块](https://www.btime.com/?from=gjl)*

      - API `https://pc.api.btime.com/btimeweb/getInfoFlow?callback=jQuery111308214331648120714_1528901698870&channel=news&request_pos=channel&citycode=local_330500_330000&sub_channel=&refresh=6&req_count=6&refresh_type=2&pid=3&from=&page_refresh_id=bdd83c10-6f19-11e8-8796-6c92bf0a9cdb&_=1528901698882`

      - ![news](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/news.png)



9. [Feature] 记住用户的 10 条搜索历史。显示给用户，可单条或全部删除。分别用 cookie 和 localStorage 实现
   - 考察：cookie、localStorage、css sprite。雪碧图如下，来自 [百度搜索](http://www.baidu.com)：
     
     ![favorite-sites](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/baidu-sprite.png)

   - hover 显示删除箭头，箭头来自雪碧图第二行右数第二个，效果图如下，结合参考第 3 点的腾讯视频效果图：

     ![favorite-sites](https://raw.githubusercontent.com/legend80s/front-end-exercise-sites/master/images/history.png)

10. [Feature] 记住用户最后选择的 tab。即当用户刷新页面后仍然会定位到最后选中的 tab。用 cookie 实现。清空缓存则默认展示第一个 tab

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

2. [Refactor] for 循环用 forEach 替换。并熟悉数组的
   - 处理方法：map reduce filter splice slice。检验习题：

     ```javascript
     // 某开发通过 shell 脚本统计了两台服务器的请求日志，并已将各台服务器的请求 IP 和相应的请求次数统计如下：
     // 服务器一
     // 10646 10.101.86.1
     // 25948 10.101.86.2
     // 服务器二
     // 25905 10.101.86.1
     //   424 10.101.86.3
     // 其中第一列是请求次数，第二列是请求 IP；
     // 接下来请你实现聚合功能：合并相同请求 IP 的出现次数，必须使用数组的 filter map reduce。
     
     // 输入字符串
     var input = `
     10646 10.101.86.1
     25948 10.101.86.2
     25905 10.101.86.1
       424 10.101.86.3
     `;
     
     // 输出
     var output = {
       "10.101.86.1": 36551,
       "10.101.86.2": 25948,
       "10.101.86.3": 424
     }
     
     // 函数签名如下
     
     /**
      * 聚合相同请求 IP 的次数
      * @param  {String} log
      * @return {Object}     
      */
     function aggregate(log) {
       // TODO 答案见最后
     }
     ```

   - 查找方法：find includes indexOf some every

3. [Refactor] 组件化。相同的重复的 HTML 结构，封装为组件。比如某个视频和某条新闻都有相似的 HTML 结构和功能
   - 重要性：为提倡“组件化优先”的框架学习打基础。
   - 重要性：组件化的目的就是 DRY 原则

4. [Performance] 防止输入频繁导致发送不必要请求，写 debounce 函数。
   - 重要性：函数式编程之高阶函数初探

5. TODO

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
   - 和 callback 比较，为什么说 Promise saves you from the callback hell？
   - 熟悉 Promise 的实例方法 catch finally 和静态方法 all race
9. [Refactor] Promise 的调用改为 aync / await。并体会其好处。

### 高级进化

#### 目标

成为一个可独当一面的职场前端。主要在发力在打包构建、框架、新思想新语言方面

1. Webpack 3，结合 babel-loader 让我们有能力用未来的技术编程 
   - TODO
   - less sass。至少会一种
   - 熟悉所有 es6 语法；知道 es7 的新特性 

2. 函数式编程
   - js 哪些方法支持函数式编程
   - 用函数式编程重构

3. 新建一个项目，用 React.js / Vue.js 重构下拉提示

4. ~~新建一个项目，用 typescript 重构~~ 了解 typescript

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

## 原则

不知者无罪，所以最后还得反复叮咛你以下几条原则：

1. Always Keep it **DRY**。代码重复的部分不断出现，那是代码“霉变”的前兆。分层思想、编程范式和设计模式会拯救你。
2. **KISS** - Keep It Simple and Stupid。简单好过复杂，不仅适用于代码，产品设计亦如此。
3. **Everything should be made as simple as possible but no simpler**。过度设计、黑魔法都是违反该原则的具体体现。不过现在的你可忽略该原则，“你长大了就会明白”原谅我一副老父亲的“嘴脸”。
4. **Readability counts**。可读性很重要。因为代码终将被后来者维护，可能是别人也可能是几个月之后的你，而且优秀的代码将会被反复咏读。当你无法轻松地向你的“伙伴”或著名的“橡皮鸭”解释某段代码的意思，或需花费很长时间（意味着代码过长，该封装为函数或模块了），或没法用语言精确地想听众描述某个变量或函数的名字（回顾下命名的艺术），你就违反了该条原则。
5. **Python 之禅**。有时间就静下心修行这部禅吧！
6. **Stay Hungry Stay Foolish**。You shall keep learning, my bro。学习各种能够带给你思想冲击的编程语言、工具、框架和编程范式等等。再培养一点点对文字、颜色、排版、布局和设计的美感就 Perfect 了，简单来说就是“知美丑”，毕竟你是前端工程师。
6. TODO。

孟子曰：“羞恶之心，人皆有之”。知道了原则还违反就该感到羞耻，这不仅是个人操守有问题，也违反了程序员的职业道德。违反原则必定累积技术债，而“出来混总是要还的”。这是我教给你的最后一条原则——**羞耻原则**。

但我们所处并非“乌托邦”，由于资源等的限制，这些原则不能完全实施，但此时仍然要保持“**羞耻心**”。这是你唯一不能放弃的原则。

我们要做一个“有礼貌、守原则、知廉耻、辨美丑”的程序员。

## 博客和网站推荐

1. [阮一峰的个人网站](http://www.ruanyifeng.com/home.html) 和他的微信公众号【阮一峰的网络日志】
2. [The HTML & CSS Security Checklist](https://www.sqreen.io/checklists/html-css-security-checklist)
3. CSS 属性不会用看这个网站 <https://cssreference.io/>
4. https://github.com/kujian/30-seconds-of-css
4. [JavaScript 的算法与数据结构](https://github.com/trekhleb/javascript-algorithms)
5. [A few HTML tips](https://hacks.mozilla.org/2016/08/a-few-html-tips/) 适合初学者
6. [Learn Vanilla JavaScript](https://github.com/snipcart/learn-vanilla-js)
7. [You Don't Know JS English Version](https://github.com/getify/You-Dont-Know-JS/blob/master/this%20%26%20object%20prototypes/ch1.md), [中文版](https://github.com/kujian/You-Dont-Know-JS/tree/1ed-zh-CN)

## 面试题

1. https://github.com/InterviewMap/CS-Interview-Knowledge-Map
2. https://github.com/yangshun/tech-interview-handbook
3. https://github.com/CyC2018/CS-Notes
4. https://yuchengkai.cn/docs/zh/frontend/

## 常见误区

1. [GET 是否可以带 Body](https://yanbin.blog/why-http-get-cannot-sent-data-with-reuqest-body/)
  - 从协议与实现的角度来说：协议并未认为 GET 带 body 是不遵循规范的，但是很多实现并不支持，故给我们一种印象 GET 不能带 body，既然实现不支持，自然推荐不带 body
  - 从缓存的角度来说：GET 被设计来用 URI 来识别资源，如果让它的请求体中携带数据，那么通常的缓存服务便失效了，URI 不能作为缓存的 Key。
  
2. TODO

## 部分答案

1. 聚合相同请求 IP 的次数

   ```javascript
   function aggregate(log) {
     return log
       .split('\n')
       .filter(s => s !== '')
       .map(s => s.trim())
       .map(s => s.split(' '))
       .reduce((acc, cur) => {
         typeof acc[cur[1]] === 'undefined' ? 
           (acc[cur[1]] = Number(cur[0])) :
           (acc[cur[1]] += Number(cur[0]));
   
         return acc;
       }, {});
   }
   ```

2. Angular 6 实现见 https://github.com/legend80s/sites-angular

3. TODO
