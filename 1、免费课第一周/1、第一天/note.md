# js是什么(javaScript)
# css做的功能js都可以做，js做的功能，css不一定能做

# web前端开发工程师
- web1.0时代 (写静态页面 2013)【网页开发】

- web2.0
    + 弱前端时代(服务器渲染)
    + 前端时代(客户端渲染)

- 全面进军移动端
- node.js


# 浏览器
- 打开控制台(右键+检查、f12、ctrl+f12)
- Elements:可以查看和修改页面的结构和样式，
- Consoles：可以运行代码，还可以打印js中的内容,可以帮助我们调试代码
- Sources：存放的是页面的静态资源
- NetWork：存放的是发送的数据请求

# 浏览器的分类(按照内核)：
谷歌(Chrome)、火狐(FireFox)、欧朋(Opera)、IE、搜狗  safari、qq浏览器、

- webkit内核(v8引擎)
 + Chrome
 + safari
 + 国产浏览器
 + 手机浏览器

- Gecko
 + FireFox

- Prosto
 + Opera

- Trident
 + IE
 + IE EDGE  (Chrome mini)


## js(javaScript)
> js作为一门前端开发语言，不仅要操作浏览器，还要操作页面中的dom元素
    - ECMAScript(3/5)[老版本]：他规定了js的语法、变量和操作语句等(ECMAScript部门的核心成员是各个浏览器的开发者)
        + ECMAScript简称ES3/5  (6/7)

    - DOM:document object model:规定了js的一些属性和方法，用来操作页面当中的dom元素
    - BOM：browser object model：规定了js的一些属性和方法，用来操作浏览器

## js中创建变量的方式
    - var创建变量(ES5)
    - let创建变量(ES6)
    - const常见常量(不许与被更改)(ES6)
    - function 创建函数变量(ES5)
    - import(ES6)
    - class(ES6)

## js的命名规范
    - 严格遵循大小写
    - 名字由数字、字母、下划、$线组成，不能以数字开头,
    - 不能以关键字和保留字作为变量名
    - 遵循驼峰命名法(名字的第一个单词首字母小写，以后每一个有意义的单词的首字母大写)

## js中的数据类型
- 基本数据类型
    + number 数字   1 12  -12  +12 12.4 0 -12.5
    + string 字符串  '1' " "  `` 把这些东西包起来的都是字符串
    + boolean 布尔  true false
    + null  空指针对象 null
    + undefined  未定义  undefined
    + Symbol 创建唯一值
- 引用数据类型
    + Object 对象
        + 普通对象  {name:12,age:13}
        + 数组  [1,2,3,'4']
        + Math 数学对象
        + 正则 /^\d{3,4}$/
        + Date的实例
    +  Function 函数
        + 普通函数
        + 类

## number 数字类型
    number的组成：
    > 有效数字： 12， 13.5， 13.4 -3， +5， 0
    > NaN(not a number) 他的意思是不是一个有效数字，但是是number数据类型的【NaN和谁都不相等，包括他自己】

### 把其他数据类型转换为数字类型 Number(val)
    - 1、把字符串转换为数字
        + 1、把字符串转换为数字，只要字符串中出现了非有效数字，那转换的结果就是NaN(数字里的第一个点和+-号不算)
        + 2、如果左右有空格，会默认把空格去掉
        + 3、空字符串里不管有没有空格转数字是0

    -2、把布尔转数字 true false
        + true转数字是 1
        + false转数字是 0

    -3、null和undefined
        + null转数字是0
        + undefined转数字是NaN
    
    > 引用数据类型转数字：先把值默认转换为字符串(浏览器内部会默认去调用toString方法)，然后在把字符串转数字

    - 4、普通对象转数字
        + 所有的普通对象转字符串都是 '[object Object]'
        + 所有的普通对象转数字都是NaN

    - 5、数组转数字
        + 数组转数字是把数组里的每一项先转字符串，然后连同逗号和转换的结果拼接起来，再去转数字
        + 空数组转字符串是空字符串

### parseInt和parseFloat 是把字符串转换为数字

    - 从左往右依次查找有效数字，一旦发现非有效数字，就立即停止查找，把之前找到的数字返回(parseInt不识别小数点，parseFloat识别一位小数点)
    - 如果输入的值不是字符串类型的，会先把值转换为字符串在运算
    
### isNaN：检测当前值是否是一个非有效数字，如果是非有效数字，就返回true，否则返回false
    - 如果你输入的不是number数据类型的值，他会默认调用Number方法，转数字，然后在检测
    - (如果检测的值是有效数字，就返回false，反之就返回true)



