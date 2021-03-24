# Html

#### 标签

##### 文档标签 

+ dcotype
  + 定义
    + 一种标准通用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义（DTD）来解析文档。
    + 直白点就是：告诉浏览器要按照什么样的规范模式解析html内容
    
  + 文档类型
    + html4
      + HTML4.01 strict 严格模式
        + 不允许使用表现性、废弃元素（如font）以及frameset
      + HTML4.01 Transitional 过渡模式
        + 允许使用表现性、废弃元素（如font），不允许使用frameset
      + HTML4.01 Frameset 框架模式
        + 允许表现性元素，废气元素以及frameset
    + xml
      + XHTML1.0 Strict 严格模式
        + 不使用允许表现性、废弃元素以及frameset。文档必须是结构良好的XML文档
      + XHTML1.0 Transitional 过渡模式
        + 允许使用表现性、废弃元素，不允许frameset，文档必须是结构良好的XMl文档
      + XHTML 1.0 Frameset 框架模式
        + 允许使用表现性、废弃元素以及frameset，文档必须是结构良好的XML文档
    + Html5
      + html5本身不基于sgml，不需要对dtd引用
    
  + 浏览器渲染模式
    + 标准模式
      + 浏览器使用W3C的标准解析渲染页面。在标准模式中，浏览器以其支持的最高标准呈现页面
    + 混杂模式
      + 浏览器使用自己的怪异模式解析渲染页面。在怪异模式中，页面以一种比较宽松的向后兼容的方式显示
    + 详细请看[模式](https://hsivonen.fi/doctype/)
    
    ```html
    // html4 严格模式
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
    // html4 过渡模式
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/transitional.dtd">
    // html4 框架模式
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/frameset.dtd">
    // xml 严格模式
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
    // xml 过渡模式
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    // xml 框架模式
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
    
    // html5 
    <!DOCTYPE html>
    ```
    
    
  
+ html
  + 定义
    + 全称为超文本标记语言，是一种标记语言。它包括一系列标签．通过这些标签可以将网络上的文档格式统一，使分散的Internet资源连接为一个逻辑整体。HTML文本是由HTML命令组成的描述性文本，HTML命令可以说明文字，图形、动画、声音、表格、链接等	
    + 整个文档的根元素，并且告知浏览器其自身是一个 HTML 文档，标签限定了文档的开始点和结束点
  + 属性manifest
    + html5引入，用于设定文档的缓存
    
    + url
      
      + 文档缓存位置
      
    + 用法
      + 绝对url
        + 指向另一个网站（比如 href="http://www.example.com/demo.appcache"）
      + 相对url
        + 指向网站内的一个文件（比如 href="demo.appcache")
      
    + 优点
      + 离线浏览 - 用户可以在离线时使用应用程序
      + 快速 - 缓存的资源可以更快地加载
      + 减少服务器加载 - 浏览器只从服务器上下载已更新/已更改的资源
      
    + 可以用于性能优化
    
      ```html
      <html mainfest="demo.appcache">
        <!-- 内容 -->
      </html>
      ```
  
+ head

  + 定义
    + 文档头部
    + 用于配置元数据
      + 文档标题 title
      + 引用文档样式 link
      + 文档内样式 style
      + 引用脚本 script
      + 不支持引用脚本 noscript
      + 定义文档配置 meta
      + 文档根Url元素 base
      +  commad - 已废弃

+ body

  + 定义
    + 文档的内容

  ```html
  <!Doctype html>
  <html>
    <head>
      <!-- 在此配置title meta link style script base noscript -->
    </head>
    <body>
      <!-- 在此输入文档主体内容 -->
    </body>
  </html>
  ```

  

##### 元标签

+ title

  + 定义
    + 文档的标题
  + 一个head中只能有一个title
  + 可以用于seo
  + 可用document.title查询

+ meta

  + 定义

    + 提供html文档的元数据

  + 属性

    + charset

      + 定义文档字符集声明，告诉文档使用哪种字符编码

        ```html
        <meta charset="utf-8" >
        ```

    + content

      + 定义
        + 与name 或 http-equiv搭配使用，包含name或http-equiv值

    + http-equiv

      + 定义编译指示指令，允许所有的值都是特定http头部的名称
      + 参数
        + expires
          + 设置网页的过期时间，过期后需要重新情求服务器
          + content 为 GMT格式时间
        + pragma
          + 设定禁止浏览器从本地机的缓存中调阅页面内容，设定后一旦离开网页就无法从Cache中再调出用法
          + content 为 no-cache
          + 注意：如此设置后，用户无法脱机浏览
        + refresh
          + 自动刷行并指向新页面
          + content 为 2; URL=http://www.xxx.com
            + 其中2为停留2秒后自动刷新到url地址
        + set-cookie
          + 如果网页过期后，存储的cookie将被删除
          + content 为cookievalue=xxx;expires=wednesday,20-jun-2007 22:33:44 GMT;path=/
            + expires必须使用GMT时间
        + window-target
          + 强制页面在当前窗口以独立页面显示
          + content为_top
            + 用来防止别人在框架里调用自己的页面
        + content-type
          + 设置页面使用的字符集
          + content 为 text/html;charset=utf-8
        + pics-label
          + 网页等级评定，在IE的intert选项中有一些内容设置，可以防止浏览一些受限制的网站，而网站的受限制级别就是通过meta属性来设置的
        + page-enter / page-exit
          + 设定进入 / 离开页面时的特殊效果
          + content 为revealTrans(duration=1.0,transtion= 12)
            + duration的值为网页动态过度的时间，单位为秒
            + transtion是过度方式，它的值为0到23，分别对应24种过度方式
              + 盒状收缩 / 盒状放射 / 圆形收缩 / 圆形放射 / 由下往上 /  由上往下 /  从左至右 / 从右至左 / 垂直百叶窗 / 水平百叶窗  / 水平格状百叶窗 / 垂直格状百叶窗 / 随意溶解  / 从左右两端向中间展开  / 从中间向左右两端展开  / 从上下两端向中间展开 / 从中间向上下两端展开 / 从右上角向左下角展开 / 从右下角向左上角展开 / 从左上角向右下角展开 /  从左下角向右上角展开 / 水平线状展开 / 垂直线状展开 / 随机产生一种过渡方式 
        + cache-control
          + 清除缓存
          + content 为no-cache
        + content-security-policy
          + 允许用户定义自己的内容策略，[内容策略](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy)主要指定允许的服务器源和脚本端点,有助于防止跨站点脚本攻击

    + name

      + 定义

        + 提供文档级别的元数据

      + 参数

        + description

          + 设置文档描述

        + author

          + 设置文档作者

        + keywords

          + 设置文档搜索关键词

        + referrer

          + 引用策略从一个文档发出请求时，是否在请求头部定义了referrer的设置, [mdn-referrer](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Referrer-Policy)

          + 内容属性分类

            + never
              + 等价no-referrer，所有请求不发送referrer
            + always
              + 等价unsafe-url, 无论是否发生协议降级，无论是本站链接还是站外链接，统统都发送 Referrer 信息。正如其名，这是最宽松而最不安全的策略
            + origin
              + same-origin
                + 对于同源的链接和引用，会发送referrer，其他的不会
              + origin
                + 会发送 referrer，但只会发送源信息。源信息包括访问协议和域名
              + strict-origin
                + 这个相当于 origin 和 no-referrer-when-downgrade 的 AND 合体。即在安全级别下降时不发送 referrer；安全级别未下降时发送源信息
                + 注意：这个是新加的标准，有些浏览器可能还不支持
              + origin-when-cross-origin
                + 相当于 origin 和 same-origin 的 OR 合体。同源的链接和引用，会发送完全的 referrer 信息；但非同源链接和引用时，只发送源信息
              + strict-origin-when-cross-origin
                + 比较复杂，同源的链接和引用，会发送 referrer。安全级别下降时不发送 referrer。其它情况下发送源信息
                + 注意：这个是新加的标准，有些浏览器可能还不支持
            + default
              + 等价no-referrer-when-downgrade, 当请求安全级别下降时不发送 referrer。目前，只有一种情况会发生安全级别下降，即从 HTTPS 到 HTTP。HTTPS 到 HTTP 的资源引用和链接跳转都不会发送 referrer

          + 设置方法

            + 在http响应头中设置referrer-policy字段
            + 通过meta设置，name为referrer，content为以上的值
            + 通过链接标签添加，如a、area、img、iframe、link、script元素的referrer policy属性
            + 其中元素 a、area、link可以在rel属性上设置为no referrer

            

        + robots

          + 设置机器人向导
          + 告诉搜索机器人那些页面需要索引，那些不需要
          + conent 参数
            + 默认值 all
              + 文件将被检索，且页面上的链接可以被查询
            + none
              + 文件将不被检索，且页面上的链接不可以被查询
            + index
              + 文件将被检索
            + noindex
              + 文件将不被检索，页面链接可以被查询
            + follow
              + 页面上链接可以查询
            + nofollow
              + 文件将不被检索，页面上的链接可以被查询

        + revisit-after

          + 通知搜索引擎多少天可以访问一次

        + copyright

          + 设置版权

        + application-name

          + 页面代表应用程序的名称

        + generator

          + 生成文档的软件包

        + website

          + 网页地址

        + date

          + 设置时间
          + scheme规定日期格式

        + viewport

          + 可以配置的移动端常用视口
          + 参数配置
            + width 
              + 宽度（数值/device-width）(默认值为980像素)
            + height
              + 高度 （数值/ device-height）
            + initial-scale
              + 初始化屏幕缩放比例, 缩放范围（>0到10）
            + minimum-scale
              + 允许用户缩放的最小比例
            + Maximum-scale
              + 允许用户缩放的最大比例
            + user-scalable
              + 用户是否可以手动缩放
                + no
                + yes

        + Internet Explorer 浏览器

          + skype_toolbar
            + 是否开启cleartype显示效果,content值为skype_toolbar_parser_compatible
            + 与http-equiv 一起使用,http-equiv值为cleartype,conent值为on
          + msapplication-TileImage
            + IE10 / window 8
            + content为图片地址
          + msapplication-TileColor
            + IE10 / window 8
            + content为十六进制颜色值，#0f0
          + msapplication-config
            + IE 11 / Windows 9.1
            + content只为xml的配置文件

        + chrome 浏览器

          + google
            + 禁止自动翻译
            + 与value一起使用，value值为no translate

        + 360 浏览器

          + renderer
            + 选择使用的浏览器解析内核
            + content值为webkit | ie-comp | ie-stand

        + Uc浏览器

          + screen-orientation
            + 将屏幕锁定在特定的方向
            + content值为landscape/portrait
          + full-screen
            + 全屏显示页面
            + content值为yes / no
          + imagemode
            + 强制图片显示，即使是"text mode"
            + content 为force
          + browsermode
            + 浏览器应用模式，默认将全屏，禁止长按菜单，禁止手势，强制图片显示
            + content 为 application
          + nightmode
            + 禁止夜间模式
            + content 为disable
          + layoutmode
            + 使用适屏模式显示
            + conent 为fitscreen
          + wap-font-scale
            + 当页面有太多文字时禁止缩放
            + content 为no

        + QQ 浏览器

          + x5-orientation
            + 锁定屏幕在特定方向
            + content 为 landscape/portrait 
          + x5-fullscreent
            + 全屏显示
            + content为true
          + x5-page-mode
            + 页面将以应用模式显示
            + content 为 app

        + Apple IOS

          + apple-tunes-app
            + 设置智能应用横幅
            + content 值为
              + app-id=APP_ID
              + affiliate-data=AFFILIATE_ID
              + app-argument=SOME_TEXT
          + format-detection
            + 禁止自动探测并格式化手机号码
            + content 值为telephone=no
          + app-mobile-web-app-capable
            + Add to Home Screen添加到主屏/ 是否启用 WebApp 全屏模式
            + content值为yes
          + apple-mobile-web-app-status-bar-style
            + 设置状态栏的背景颜色,只有在 "apple-mobile-web-app-capable" content="yes" 时生效
            + content值为颜色值（如black）
          + apple-mobile-web-app-title
            + 添加到主屏后的标题
            + content值为app title

        + 不支持viewport浏览器

          + handhelFriendly

        + 微软老师浏览器

          + mobileOptimized

        

    ```html
    <!-- 常用 -->
    <meta name="description" content="this is a demo page">
    <meta name="author" content="lxl">
    <meta name="keywords" content="test,demo,lxl">
    <meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0, user-scalable=no">
    
    <!-- IE 浏览器 -->
    <!-- 优先使用最新的ie版本 -->
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <!-- 是否开启cleartype显示效果 -->
    <meta http-equiv="cleartype" content="on">
    <meta name="skype_toolbar" content="skype_toolbar_parser_compatible">
    <!-- Pinned Site -->
    <!-- IE 10 / Windows 8 -->
    <meta name="msapplication-TileImage" content="pinned-tile-144.png">
    <meta name="msapplication-TileColor" content="#009900">
    <!-- IE 11 / Windows 9.1 -->
    <meta name="msapplication-config" content="ieconfig.xml">
    
    <!-- chrome 浏览器 -->
    <!-- 禁止自动翻译 -->
    <meta name="google" value="notranslate">
    
    <!-- 360 浏览器 -->
    <!-- 选择使用的浏览器解析内核 -->
    <meta name="renderer" content="webkit|ie-comp|ie-stand">
    
    <!-- UC 浏览器 -->
    <!-- 将屏幕锁定在特定的方向 -->
    <meta name="screen-orientation" content="landscape/portrait">
    <!-- 全屏显示页面 -->
    <meta name="full-screen" content="yes">
    <!-- 强制图片显示，即使是"text mode" -->
    <meta name="imagemode" content="force">
    <!-- 应用模式，默认将全屏，禁止长按菜单，禁止手势，标准排版，强制图片显示。 -->
    <meta name="browsermode" content="application">
    <!-- 禁止夜间模式显示 -->
    <meta name="nightmode" content="disable">
    <!-- 使用适屏模式显示 -->
    <meta name="layoutmode" content="fitscreen">
    <!-- 当页面有太多文字时禁止缩放 -->
    <meta name="wap-font-scale" content="no">
    
    <!-- QQ 手机浏览器 -->
    <!-- 锁定屏幕在特定方向 -->
    <meta name="x5-orientation" content="landscape/portrait">
    <!-- 全屏显示 -->
    <meta name="x5-fullscreen" content="true">
    <!-- 页面将以应用模式显示 -->
    <meta name="x5-page-mode" content="app">
    
    <!-- Apple iOS -->
    <!-- Smart App Banner -->
    <meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">
    <!-- 禁止自动探测并格式化手机号码 -->
    <meta name="format-detection" content="telephone=no">
    <!-- Add to Home Screen添加到主屏 -->
    <!-- 是否启用 WebApp 全屏模式 -->
    <meta name="apple-mobile-web-app-capable" content="yes">
    <!-- 设置状态栏的背景颜色,只有在 “apple-mobile-web-app-capable” content=”yes” 时生效 -->
    <meta name="apple-mobile-web-app-status-bar-style" content="black">
    <!-- 添加到主屏后的标题 -->
    <meta name="apple-mobile-web-app-title" content="App Title">
    
    <!-- 针对手持设备优化，主要是针对一些老的不识别viewport的浏览器，比如黑莓 -->
    <meta name="HandheldFriendly" content="true">
    
    <!-- 微软的老式浏览器 -->
    <meta name="MobileOptimized" content="320">
    
    <!-- Google Android -->
    <!-- 添加到主屏 -->
    <meta name="mobile-web-app-capable" content="yes">
    <!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->
    
    <!-- 比较少用 -->
    <meta name="generator" conent="FrontPage4.0">
    <meta name="application-name" conent="typora">
    <meta name="revisit-after" conent="7 days">
    <meta name="copyright" conent="xxx科技公司">
    <meta name="robots" conent="all">
    <meta name="website" conent="http://www.xxx.com">
    <!-- 暗黑模式 -->
    <meta name="color-scheme" value="light dark">
    <meta name="date" content="2009-01-02" scheme="YYYY-MM-DD">
    <meta name="referrer" content="no-referrer">
    <meta name="theme-color" content="#E64545">
    
    <!-- chrome 浏览器 -->
    <!-- 优先使用最新的chrome版本 -->
    <meta http-equiv="X-UA-Compatible" content="chrome=1" >
    
    <meta http-equiv="expires" content="Wed, 20 Jun 2007 22:33:00 GMT"＞
    <meta http-equiv="refresh" content="2；URL=http://www.net.cn/" >
    <meta http-equiv="pragma" content="no-cache">
    <meta http-equiv="Set-Cookie"content="cookievalue=xxx;expires=Wednesday, 20-Jun-2007 22:33:00 GMT； path=/">
    <meta http-equiv="Window-target"content="_top">
    <meta ttp-equiv="content-Type"content="text/html; charset=gb2312">
    <meta http-equie="Pics-label"  content="">
    <meta http-equie="Page-Enter"  content="revealTrans(duration=1.0,transtion= 12)">
    <meta http-equie="Page-Exit" content="revealTrans(duration=1.0,transtion= 12)">
    <meta http-equie="cache-control"  content="no-cache">
      
    ```

    

+ [link](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link)

  + 定义

    + 外部资源链接元素
    + 常用于链接样式表和站点图标

  + 属性

    + href
      + 指定链接资源的url,url可以是相对或者绝对的
    + rel
      + 指定类型
      + 值类型
        + icon - 网站图标链接
        + apple-touch-icon-precomposed 
          + 苹果上图标
          + 相关配置
            + sizes 
              + 图标大小
            + type
              + 链接资源的MIME类型
        + preload
          + 浏览器应预加载该资源
      + media
        + 设置媒体类型或查询
        + 值类型
          + print
            + 打印配置
          + screen
            + 媒体查询，指定使用的样式表条件
          + aural
          + brille
      + as
        + 特定内容被获取的属性，在rel设置为preload是使用
        + 类型
          + 字体
            + font
          + 声音
            + audio
          + 视频
            + video
          + 文档
            + iframe
          + 嵌入元素
            + embed
          + 图像
            + img
            + svg
          + 目的
            + object
          + 脚本
            + script
      + crossorigin
        + 是否通过cors获取资源，[cors](https://developer.mozilla.org/en-US/docs/Glossary/CORS)确定浏览器是否阻止前端JavaScrip代码访问跨域请求的响应
        + 值类型
          + anonymous
            + 执行跨域请求，但没有发送凭据(cookie，X.509证书或HTTP Basic身份验证)
          + use-credentials
            + 执行跨域请求已经发送的凭证(cookie，X.509证书或HTTP Basic身份验证)
    + disabled
      + 当rel为stylesheet止，disabled布尔值所描述的样式表是否应该被加载并应用到该文档，为false时按需加载
    + hreflang
      + 指定链接资源的语言，仅在有href属性时使用
    + imagesizes
      + 预加载图片时使用，用于rel为preload且as为image使用，设置图片尺寸[sizes](https://html.spec.whatwg.org/multipage/images.html#sizes-attribute)
    + Imagesrcset
      + 预加载图片时使用，用于rel为preload且as为image使用，设置图片来源[srcset](https://html.spec.whatwg.org/multipage/images.html#srcset-attribute)
    + integrity
      + 包含内联元数据，浏览器使用来验证所获取的资源是否已交付
    + prefetch
      + 标识下一个导航可能需要的资源，并且用户代理应检索资源
    + referrerpolicy
      + 指示在获取资源时使用哪个引荐资来源网址
      + 值类型
        + no-referrer
          + 表示referer将不发送标头
        + no-referrer-when-downgrade
          + referer在导航到没有TLS的来源时不会发送任何报头
        + origin
          + 引荐来源网址将是页面的来源
        + origin-when-cross-origin
          + 导航到其他来源仅限于方案
        + unsafe-url
          + 引荐来源网址将包含来预案和路径（不包括片段，密码或用户名）
    + title
      + 在link元素上有特殊的语义，当用于时，`<link rel="stylesheet">`它定义[首选样式表或备用样式表](https://developer.mozilla.org/en-US/docs/Web/CSS/Alternative_style_sheets)。错误地使用它可能会[导致样式表被忽略](https://developer.mozilla.org/en-US/docs/Correctly_Using_Titles_With_External_Stylesheets)
    + type
      + 定义MIME类型
      + 值类型
        + text/html
        + text/css
    + methods
      + 提供有关可能在对象上执行的功能信息
    + target
      + 定义具有已定义链接关系或将显示任何链接资源呈现的框架或窗口
    + charset
      + 定义链接资源的字符编码
    + rev
      + 显示该属性定义的当前文档于链接文档的关系

    ```html
    <link href="style.css" rel="stylesheet">
    <link href="default.css" rel="stylesheet" title="Default Style">
    <link href="fancy.css" rel="alternate stylesheet" title="Fancy">
    <link href="basic.css" rel="alternate stylesheet" title="Basic">
    <!-- third-generation iPad with high-resolution Retina display: -->
    <link rel="apple-touch-icon-precomposed" sizes="144x144" href="favicon144.png">
    <!-- iPhone with high-resolution Retina display: -->
    <link rel="apple-touch-icon-precomposed" sizes="114x114" href="favicon114.png">
    <!-- first- and second-generation iPad: -->
    <link rel="apple-touch-icon-precomposed" sizes="72x72" href="favicon72.png">
    <!-- non-Retina iPhone, iPod Touch, and Android 2.1+ devices: -->
    <link rel="apple-touch-icon-precomposed" href="favicon57.png">
    <!-- basic favicon -->
    <link rel="icon" href="favicon32.png">
    <link href="print.css" rel="stylesheet" media="print">
    <link href="mobile.css" rel="stylesheet" media="all">
    <link href="desktop.css" rel="stylesheet" media="screen and (min-width: 600px)">
    <link href="highres.css" rel="stylesheet" media="screen and (min-resolution: 300dpi)">
    <script>
    var myStylesheet = document.querySelector('#my-stylesheet');
    
    myStylesheet.onload = function() {
      // Do something interesting; the sheet has been loaded
    }
    
    myStylesheet.onerror = function() {
      console.log("An error occurred loading the stylesheet!");
    }
    </script>
    
    <link rel="stylesheet" href="mystylesheet.css" id="my-stylesheet">
    ```

    

+ [style](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style)

  + 定义

    + 包含文档的文档或者部分样式信息

  + 属性

    + type
      + 将样式语言定义为MIME类型
    + media
      + 定义将样式应用于哪种媒体，值时一个[媒体查询](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)如果缺少则为默认all
    + nonce
      + 用于在[style-src Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/style-src)中将内联样式列入白名单的密码随机数（一次使用的数字）
    + title
      + 指定[替代样式表](https://developer.mozilla.org/en-US/docs/Web/CSS/Alternative_style_sheets)
    + scoped
      + 指定样式仅适用于其父项和子项的元素

    ```html
    <!doctype html>
    <html>
    <head>
      <style>
        p {
          color: white;
          background-color: blue;
          padding: 5px;
          border: 1px solid black;
        }
      </style>
      <style media="all and (max-width: 500px)">
        p {
          color: blue;
          background-color: yellow;
        }
      </style>
    </head>
    <body>
      <p>This is my paragraph.</p>
    </body>
    </html>
    ```

    

+ [script](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script) 

  + 定义

    + 用于嵌入的可执行代码或数据，通常嵌入或引用JavaScript代码

  + 属性

    + async
      + 在经典脚本上存在属性，则将并行获取脚本进行解析，在可用时立即进行评估
      + 在模块脚本上，则脚本及其所有依赖项将在延迟队列中执行，在解析时并行获取它们并对其进行评估
    + crossorigin
      + 允许对单独域的静态媒体的站点进行错误日志记录详细参考[CORS设置属性](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/crossorigin)
    + defer
      + 向浏览器指示脚本应在文档解析后但在fire之前执行[DOMContentLoaded](https://developer.mozilla.org/en-US/docs/Web/API/Window/DOMContentLoaded_event)
      + 具有该属性时将按照它们在文档中出现的顺序执行
      + 可以消除阻止解析器的JavaScript
    + integrity
      + 包含内联元数据，用户代理可使用这些内联元数据来验证获取的资源是否已交付而没有意外的操作。请参阅子[资源完整性](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity)
    + nomodule
      + 为了指示该脚本不应在支持[ES2015模块的](https://hacks.mozilla.org/2015/08/es6-in-depth-modules/)浏览器中执行—实际上，该脚本可用于向不支持模块化JavaScript代码的旧版浏览器提供后备脚本
    + nonce
      + 加密随机数（一次使用的数字），用于将[script-src Content-Security-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src)中的[脚本](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src)列入白名单。服务器每次发送策略时都必须生成一个唯一的随机数值。提供一个无法猜测的随机数非常重要
    + referrerpolicy
      + 指示在获取脚本或脚本获得资源时发送哪个[引荐来源网址](https://developer.mozilla.org/en-US/docs/Web/API/Document/referrer)
      + 值类型
        + no-referrer
          + 表示referer将不发送标头
        + no-referrer-when-downgrade
          + referer在导航到没有TLS的来源时不会发送任何报头
        + origin
          + 引荐来源网址将是页面的来源
        + origin-when-cross-origin
          + 导航到其他来源仅限于方案
        + unsafe-url
          + 引荐来源网址将包含来预案和路径（不包括片段，密码或用户名）
    + src
      + 指定外部脚本的额uri, 可以直接作用在文档中嵌入脚本的替代方法
    + type
      + 表示脚本的类型
      + 类型
        + 省略或Javascript MIME类型
          + 默认是JavaScript
        + module
          + 代码被视为JavaScript模块
        + 其他值
          + 嵌入的内容被视为浏览器不会处理的数据
    + charset
      + 指定字符集编码
    + language
      + 指定语言类型

    ```html
    <!-- 默认类型JavaScript -->
    <script src="javascript.js"></script>
    <!-- 在文档中直接输入 -->
    <script>
      alert("Hello World!");
    </script>
    <!-- 模块类型 -->
    <script type="module" src="main.js"></script>
    <script nomodule src="fallback.js"></script>
    
    <!-- Generated by the server -->
    <script id="data" type="application/json">{"userId":1234,"userName":"John Doe","memberSince":"2000-01-01T00:00:00.000Z"}</script>
    
    <!-- Static -->
    <script>
      const userInfo = JSON.parse(document.getElementById("data").text);
      console.log("User information: %o", userInfo);
    </script>
    ```

    

+ noscript

  + 如果页面上的脚本类型不受支持或者脚本在浏览器当前处于关闭状态插入的html部分

    ```html
    <noscript>
      <!-- anchor linking to external file -->
      <a href="https://www.mozilla.com/">External Link</a>
    </noscript>
    <p>Rocks!</p>
    <!-- 启动脚本时 -->
    <p>
      Rocks
    </p>
    <!-- 禁用脚本时 -->
    <p>
      <a href="">External link</a>
    </p> 
    ```

    

+ [base](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/base)

  + 定义

    + 用于指定一个文档中包含所有相对url的根url，一份中只能有一个base元素
    + 可用document.baseURI查询

  + 属性

    + href

      + 在文档用于相对url的基本url, 允许使用绝对和相对url

    + target

      + 一个**关键字**或**作者定义的名称**默认的[浏览器上下文](https://developer.mozilla.org/en-US/docs/Glossary/Browsing_context)来显示导航从结果中[a](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)，[area](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/area)或[form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)元素没有明确的`target`属性
      + 值类型
        + _self
          + 在当前浏览器上下文中红显示结果
        + _blank
          + 新打开的浏览器上下文中显示结果
        + _parent
          + 如果在当前框架内，则在浏览器的父浏览器上下文中显示结果
        + _top
          + 在最顶部的浏览器上下文中显示结果

      ```html
      <base href="https://www.example.com/">
      <base target="_blank">
      <base target="_top" href="https://example.com/">
      ```

+ command 废弃

  + 定义
    + 表示一个命令用户可以调用
  + 属性
    + checked
      + 是否选择了该命令
    + disabled
      + 命令不可用
    + icon
      + 给出代表命令的图片
    + label
      + 显示给用户的命令名称
    + radiogroup
      + 提供的命令组名称
    + type
      + 指示命令类型

##### 语义标签

+ [header](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/header)
  + 定义
    + 用于展示介绍性的内容，通常包含一组介绍性或者辅助导航的使用元素
  + 使用时不能作为address、footer或者另一个header的子元素
+ [footer](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/footer)
  + 定义
    + 章节内容或根节点元素的页脚
  + 使用时不能作为address、header或者另一个footer的子元素
+ [aside](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/aside)
  + 定义
    + 侧边栏或者标注框，被默认为是独立于该内容的有一部分并且可以被单独拆出来的
  + 使用时不能时address的子元素
+ [nav](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/nav)
  + 定义
    + 在文档或其他文档中提供文档链接，通常用于导航 菜单 索引
+ [section](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/section)
  + 定义
    + 在html文档中的独立部分，没有更具体的语义元素表示，通常会包含一个标题
  + 使用
    + 通过是否包含一个标题作为子节点来辨识section,如果要表示文章整个部分可以使用article
    + 不能section作为一个普通的容器使用，应该用户文档大纲中
    + Section嵌套时自动给h1-h6标题自动降级
+ [article](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article)
  + 定义
    + 表示文档、页面、应用或网站的独立结构可以成为独立分配或复用的结构，可以是论坛帖子、杂志、新闻文章、博客、用户提交的评论、交互式组件或者其他独立的内容项目
  + 使用时
    + 不能成为address的子元素
    + 通常包括标题（h1-h6）、可以内嵌article
+ [address](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/address)
  + 定义
    + 表示提供某个人或者某个组织的信息，适用于上下文的背景信息，可以是必要的任意一种联系方式
  + 使用
    + 不能嵌套address
    + 不能是header、footer、h1-h6、article、aside、section、nav的子元素
+ [time](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/time)
  + 定义
    + 表示24小时制时间或者公历日期
  + 属性
    + datetime
      + 表示此元素的时间和日期并且属性值必须时一个有效的日期格式并报行时间
    + pubdate
      + 涉及和讨论中
+ [figure](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/figure)
  + 定义
    + 一段独立的内容，通常与说明元素（figcaption）配合使用，作为一个独立的引用单元
    + 在文档中用于引用的图片、插图、表格、代码段等
+ [figcaption](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/figcaption)
  + 定义
    + 与相关图片的说明/标题，用于描述其父节点figure的其他数据
+ [dialog](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dialog)
  + 定义
    + 表示一个对话框或者其他交互式组件
  + 属性
    + open
      + 用于指定对话框是否激活和能互动的，如果没有设置open属性，表示不显示给用户
      + 
+ [summary](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/summary)
  + 定义
    + 用作一个details元素的一个内容的摘要、标题或者图例
+ [bdi](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/bdi)
  + 定义
    + 双向隔离元素，告诉浏览器的双向算法将其包含的文本与周围的文本隔离
  + 属性
    + dir
      + dir属性不继承父元素，如果没有设置，默认值为auto,以便浏览器根据元素内容决定元素内容的方向
+ [a](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a)
  + 定义
    + 创建通向其他网页、文件、同一页面内的位置、电子邮件地址或者任何其他url的超链接
  + 属性
    + download
      + 指示浏览器下载url
      + 提示用户将其保存为本地文件
    + href
      + 包含超链接指向的url或者url片段
    + hreflang
      + 属性用于指定链接文档的人类语言
    + ping
      + 包含一个空格分隔的url列表，当超链接超时将由浏览器在后台发送带有正文ping的post请求，常用于跟踪
    + referrerpolicy
      + 表明在获取url时发送那个提交者
      + 值类型
        + no-referrer
          + 表示referer将不发送标头
        + no-referrer-when-downgrade
          + referer在导航到没有TLS的来源时不会发送任何报头
        + origin
          + 引荐来源网址将是页面的来源
        + origin-when-cross-origin
          + 导航到其他来源仅限于方案
        + unsafe-url
          + 引荐来源网址将包含来预案和路径（不包括片段，密码或用户名）
    + rel
      + 指定目标对象到链接对象的关系
    + target
      + 指定了在哪个地方显示链接的资源，
      + 值类型
        + _self
          + 在当前页面加载
        + _blank
          + 新窗口打开
        + _parent
          + 加载响应资源到父框架集中，如果没有parent框架或者浏览器上下文，行为方式与_self相同
        + _top
          + html4加载的响应成完整的，原来的窗口取消其他iframe,html5中加载响应进入顶层浏览器上下文，如果没有parent框架或者浏览上下文，行为方式与_self相同
      + type
        + 指定一个MIMEtype链接目标形式的媒体类型
      + charset
        + 设置字符集
      + coords
        + 只用于html4,html5已废弃
        + 使用逗号分隔的数字列表来定义对象在页面上的坐标
      + name
        + 只用于html4,html5已废弃
        + 定义锚点位置时必须的
      + rev
        + 只用于html4,html5已废弃
        + 指定当前文档和被链接文档的关系
      + shape
        + 用于定义个可选的超链接相关的数字来创建图像映射区域
+ [p](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p)
  + 定义
    + 文本段落
+ [progress](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/progress)
  + 定义
    + 显示一项任务的完成进度
  + 属性
    + max
      + 描述了元素表示任务一共需要完成多少工作
    + value
      + 表示当前该进度条已完成的工作量
+ meter
  + 定义
    + 显示已知范围的标量值或者分数值
  + 属性
    + value
      + 当前显示的值
    + min
      + 值域的最小边界值
    + max
      + 值域的最大边界值
    + low
      + 定义了低值区间的上限值，值必须比最小值属性大，并且不能超过high值和最大值
    + high
      + 定义了高值区间的下限值，值必须比最大值属性小并且必须大于low值和最小值
    + optimum
      + 用来指示最优/最佳取值
    + form
      + 将本元素与对应的form元素关联
+ [h1-h6](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Heading_Elements)
  + 定义
    + 六个不同级别的标题，h1最高，h6最低
+ [hgroup](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/hgroup)
  + 定义
    + 表示文档章节所属的多级别目录，可以将多个h1-h6标签组合在一起
+ [hr](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/hr)
  + 定义
    + 段落元素之间的主题转换
  + 属性
    + align
      + 设置对齐方式，默认为left
    + color
      + 设置分割线颜色（颜色名或者十六进制颜色）
    + noshade
      + 去除阴影
    + size
      + 设置像素高度
    + width
      + 使用像素或者百分比设置宽度

##### 无语义标签

+ [div](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/div)
  + 定义
    + 通用型流内容容器，在不使用css的情况下对内容和布局没有任何影响
+ [span](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/div)
  + 定义
    + 短语内容的通行内容器，没有特殊寓意
+ [br](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/br)
  + 定义
    + 在文本中生成换行符号
+ [pre](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/pre)
  + 定义
    + 预定义格式文本
  + 属性
    + cols
      + 定义每行的最大符数
    + width
      + 包含每行的最大字符数
    + wrap
      + 提示溢出怎样发生
    + 

##### 表格标签

+ [table](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/table)
  + 定义
    + 二维数据表格
  + 属性
    + align
      + 设置表格如何对齐
      + 值类型
        + left
        + center
        + right
    + bgcolor
      + 表格背景颜色（十六进制颜色）
    + border
      + 表格边框大小
    + cellpadding
      + 定义表格单元的内容和边框之间的空间
    + cellspacing
      + 定义表格单元之间空间的大小
    + frame
      + 包围在表格周围的框架的哪个边必须显示
    + rules
      + 在一个表格中规则的显示位置
      + 值
        + none
          + 默认值 
        + groups 
          + 显示在行组
        + rows
          + 使规则在行之间显示
        + columns
          + 使规则在列之间显示
        + all
          + 使规则在列和行之间显示
    + summary
      + 定义替代文本，当表格无法在用户代理中显示的时候用来描述表格
    + width
      + 定义表格宽度
    + 
+ [tr](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tr)
  + 定义
    + 表格中的行
  + 属性（基本都废弃不用）
    + align
    + bgcolor
    + char
    + charoff
    + valign
    + 
+ [td](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/td)
  + 定义
    + 包含数据的表格单元格
  + 属性
    + bgcolor
      + 设置表格单元背景颜色（颜色名或者十六进制颜色）
    + colspan
      + 扩展列的单元格
    + headers
      + 以空格分隔的字符串列表
    + rowspan
      + 扩展行的单元格
+ [th](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/th)
  + 定义
    + 表格内的表头单元格
  + 属性
    + abbr
      + 关于单元格内容的简单的介绍
    + align
      + 指定单元格内容的水平对齐方式
      + 值类型
        + left
        + center
        + right
        + justify
        + char
      + 
    + axis
      + 一个空间分隔的字符串的列表.每个字符串是一组单元格的ID
    + bgcolor
      + 背景颜色设置
    + char
      + 其值包含一个(.)来排列数字或者货币值
    + charoff
      + 列数据移到char属性指定字母的右边
    + colspan
      + 一个正整数表示了每单元格中扩展列的数量
    + headers
      + 一个空间分隔的字符串的列表, 每个与其他[th](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/th)元素相关联的id属性一一对应
    + rowspan
      + 一个正整数表示了每单元格中扩展列的数量
    + scope
      + 定义了表头元素 (在[th](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/th)中定义) 关联的单元格
        + row
          + 表头关联一行中所有的单元格
        + col
          + 表头关联一列中所有的单元格
        + rowgroup
          + 表头属于一个行组并与其中所有单元格相关联
        + colgroup
          + 表头属于一个列组并与其中所有单元格相关联
        + auto
          + 
    + valign
      + 单元格内文本的垂直对齐方式
    + width
      + 定义一个期望的单元格宽
+ [thead](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/thead)
+ [tbody](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tbody)
+ [tfoot](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tfoot)

##### 列表标签

+ ul
+ Li
+ ol
+ Dl
+ dt
+ dd

##### 表单标签

+ from
+ input
+ button
+ textera
+ Select

##### 辅助标签

+ em
+ i
+ s
+ b
+ strong
+ mark
+ u
+ ruby
+ rt
+ rp
+ wbr

##### 音视频标签

+ video
+ audio

##### 图片标签



#### 语法







