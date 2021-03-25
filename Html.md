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
+ [menu](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menu)
  + 定义
    + 包含菜单项内容，表示项的无序列表
  + 属性
    + label
      + 显示给用户的菜单名称
    + type
      + 指定菜单类型
      + 值类型
        + context
          + 表示弹出菜单
        + toolbar
          + 指示工具栏状态
    + 

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
  + 定义
    + 定义表格的列头行
  + 属性
    + align
      + 定义单元格内容的水平对齐方式
      + 值类型
        + left
          + 默认值
        + center
          + 居中
        + right
          + 居右
        + justify
          + 在文本内容中插入空格，以便在单元格中使用内容合理
        + char
          +  将文字内容对齐到由char和charoff属性定义的具有最小偏移量的特殊字符上
    + bgcolor
      + 定义列的每个单元格的背景色，值通常设置为颜色名或者十六进制颜色值（#开头）
      + 非标准属性，在某些版本的Ie中实现
    + char
      + 用于设置字符以对齐列中的单元格
      + 属性已在html5废弃
    + charoff
      + 指示从char属性指定的对齐字符偏移列数据的字符数
    + valign
      + 定义表格标题的每一行单元格中文本的垂直对齐方式
      + 值类型
        + baseline
          + 将使用文本尽可能的靠近单元格底部，
        + bottom
          + 使文本尽可能接近单元格的底部
        + middle
          + 使文本在单元格中居中
        + top
          + 使文本尽可能地靠近单元格的顶部
+ [tbody](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tbody)
  + 定义
    + 表示表格的主体，包含一组表中的行元素tr
  + 属性
    + align
      + 定义单元格内容的水平对齐方式
      + 值类型
        + left
          + 默认值
        + center
          + 居中
        + right
          + 居右
        + justify
          + 在文本内容中插入空格，以便在单元格中使用内容合理
        + char
          +  将文字内容对齐到由char和charoff属性定义的具有最小偏移量的特殊字符上
    + bgcolor
      + 定义列的每个单元格的背景色，值通常设置为颜色名或者十六进制颜色值（#开头）
      + 非标准属性，在某些版本的Ie中实现
    + char
      + 用于设置字符以对齐列中的单元格
      + 属性已在html5废弃
    + charoff
      + 指示从char属性指定的对齐字符偏移列数据的字符数
    + valign
      + 定义表格标题的每一行单元格中文本的垂直对齐方式
      + 值类型
        + baseline
          + 将使用文本尽可能的靠近单元格底部，
        + bottom
          + 使文本尽可能接近单元格的底部
        + middle
          + 使文本在单元格中居中
        + top
          + 使文本尽可能地靠近单元格的顶部
+ [tfoot](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tfoot)
  + 定义
    + 一组行总结的表的列
  + 属性
    + align
      + 定义单元格内容的水平对齐方式
      + 值类型
        + left
          + 默认值
        + center
          + 居中
        + right
          + 居右
        + justify
          + 在文本内容中插入空格，以便在单元格中使用内容合理
        + char
          +  将文字内容对齐到由char和charoff属性定义的具有最小偏移量的特殊字符上
    + bgcolor
      + 定义列的每个单元格的背景色，值通常设置为颜色名或者十六进制颜色值（#开头）
      + 非标准属性，在某些版本的Ie中实现
    + char
      + 用于设置字符以对齐列中的单元格
      + 属性已在html5废弃
    + charoff
      + 指示从char属性指定的对齐字符偏移列数据的字符数
    + valign
      + 定义表格标题的每一行单元格中文本的垂直对齐方式
      + 值类型
        + baseline
          + 将使用文本尽可能的靠近单元格底部，
        + bottom
          + 使文本尽可能接近单元格的底部
        + middle
          + 使文本在单元格中居中
        + top
          + 使文本尽可能地靠近单元格的顶部

##### 列表标签

+ [ul](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)
  + 定义
    + 并以的物品典型呈现为项目符号列表的无序列表
  + 属性
    + compact
      + 设置列表应以紧凑的样式呈现
    + type
      + 设置项目符号样式
      + 值类型
        + circle
        + disc
        + square
        + triangle
          + 需要注意浏览器兼容问题
+ [li](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)
  + 定义
    + 用在列表中表示的项，必须包含在ul/ol/menu
  + 属性
    + value
      + 整数属性指示ol元素定义列表项的当前序号，
    + type
      + 定义编号类型
      + 值类型
        + a
          + 小写字母
        + A
          + 大写字母
        + i
          + 小写罗马数字
        + I
          + 大写罗马数字
        + 1
          + 数字
+ [ol](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)
  + 定义
    + 定义有序列表，呈现为编号列表
  + 属性
    + reversed
      + 指定列表的项以相反的顺序排列，从高到低
    + start
      + 列表项从其开始计数的整数，从指定的值开始排列
    + type
      + 设置编号类型
      + 值类型
        + a
          + 小写字母
        + A
          + 大写字母
        + i
          + 小写罗马数字
        + I
          + 大写罗马数字
        + 1
          + 数字
+ [dl](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl)
  + 定义
    + 一个描述列表，元素包含一组术语（dt,dd）
+ [dt](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dt)
  + 定义
    + 指定的描述或定义列表的术语,必须使用在dl元素中，dt元素后跟一个dd
+ [dd](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd)
  + 定义
    + 描述详细内容
  + 属性
    + nowrap
      + 设置元素内容是否换行，默认值为no，设置为yes,文本将不换行

##### 表单标签

+ [form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)

  + 定义
    + 用于提交信息的交互式控件的文档部分
  + 属性
    + accept
      + 服务器接受的逗号分隔，已废弃
    + accept-charset
      + 服务器接受的以空格分隔的字符编码，浏览器将按照列出的顺序使用他们
    + autocapitalize
      + ios safari使用的非标准属性，用于控制文本表单元素的应该如何自动大写，
      + 值类型
        + none
          + 无自动大写
        + sentences
          + 将每个句子的首字母大写
        + words
          + 将每个单词的首字母大写
        + characters
          + 大写所有字符即大写
    + autocomplete
      + 指示输入元素默认情况下是否可以由浏览器自动完成其值
      + 值类型
        + off
          + 浏览器可能不回自动完成输入
        + on
          + 浏览器可能自动完成输入
    + name
      + 表单名称
    + rel
      + 根据值穿件超链接或者注释
  + 提交属性
    + action
      + 处理表单提交的url
    + enctype
      + 表单提交的MIME类型
      + 为post时值类型
        + application/x-www-form-urlencoded 
          + 默认值
        + multipart/form-data
          + 如果表单包含input带有的元素，使用此选项type=file
        + text/plain
          + html5引入用于调试目的
    + methods
      + 提交表单所用http方法
      + 值类型
        + post
          + 为请求正文发送
        + get
          + 表单数据附加到actions带有？分隔符URL上时
        + dialog
          + 当表单位于dialog内时，关闭提交对话框
    + novalidate
      + 布尔值属性表示在提交表单时不应验证表单，默认验证
    + target
      + 提交表单后在何处显示响应
      + 值类型
        + _self
          + 加载到与当前浏览上下文相同的浏览器上下文中
        + _blank
          + 加载到新的未命名浏览上下文中
        + _parent
          + 加载到当前浏览器的父浏览器上下文中，如果没有父母行为与_self相同
        + _top
          + 加载到顶级浏览上下文中，如果没有父母行为与_self相同
    + 

+ [input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

  + 定义

    + 用于接受来自用户的数据，以创建基于web的表单交互式控件

  + 属性

    + accept

      + file该accept属性仅对输入类型有效，定义了在file上载空间中可以选择的文件类型

    + alt

      + image该alt属性仅对按钮有效，该属性为图像提供了替代文本，在图像丢失或者加载失败时显示文本alt

    +  autocomplete

      + 该属性以空格分隔的字符串作为其值,输入应提供的自动完成功能的类型，自动完成的一种典型实现时调用在同一输入字段中输入的先前值，可以存在更富在形式的自动完成，参考[HTML自动完成属性](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete)
      + 值类型
        + hidden
        + text
        + search
        + url
        + tel
        + email
        + date
        + month
        + week
        + time
        + datetime-local
        + number
        + range
        + color
        + password

    + autofocus

      + 布尔值，存在时在页面完成加载时输入应自动获得焦点，多个元素存在时，默认第一个获得焦点

    + capture

      + `file`该`capture`属性在HTML Media Capture规范中引入，并且仅对输入类型有效，该属性定义了应使用哪种媒体（麦克风，视频或摄像机）来捕获新文件，以便`file`在支持方案中使用上载控件进行上载。请参阅[文件](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file)输入类型

    + checked

      + 在类型为radio和checked时有效，checked是布尔值

    + dirname

      + 提交元件的方向性的，在input类型为text和search输入类型时有效

    + disabled

      + 布尔值，设置了禁止用户输入

    + form

      + 字符串，指定form与输入关联的元素

    + formaction

      + 仅对image和submit输入类型有效，参考[提交](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit)

    + formenctype

      + 仅对image和submit输入类型有效，参考[提交](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit)

    + formmethod

      + 仅对image和submit输入类型有效，参考[提交](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit)

    + formnovalidate

      + 仅对image和submit输入类型有效，参考[提交](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit)

    + formtarget

      + 仅对image和submit输入类型有效，参考[提交](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit)

    + height

      + `image`仅对输入按钮有效，`height`是显示以表示图形提交按钮的图像文件的高度。请参阅[图像](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/image)输入类型

    + id

      + 全局属性对所有元素（包括所有输入类型）均有效，它定义一个唯一标识符（ID），该标识符在整个文档中必须是唯一的。其目的是在链接时识别元素。该值用作[label](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label)的`for`属性值，以将标签与表单控件链接。请参阅[label](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label)

    + inputmode

      + 全局值对所有元素均有效，它为浏览器提供了有关在编辑此元素或其内容时要使用的虚拟键盘配置类型的提示。值包括none，text，tel，url，email，numeric，decimal，和search

    + list

      + 赋予`list`属性的值应该是位于同一文档[`id`](https://developer.mozilla.org/en-US/docs/Web/API/Element/id)中的[``](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist)元素的。会``提供预定义值的列表，以建议用户进行此输入。[`type`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-type)建议选项中不包括列表中与兼容的所有值。提供的值是建议而不是要求：用户可以从此预定义列表中选择或提供其他值。有效的`text`，`search`，`url`，`tel`，`email`，`date`，`month`，`week`，`time`，`datetime-local`，`number`，`range`，和`color`
      + `list`属性不被支持`hidden`，`password`，`checkbox`，`radio`，`file`，或任何按钮类型。
      + 参见[datalist](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist)元素。

    + max

      + 有效期`date`，`month`，`week`，`time`，`datetime-local`，`number`，和`range`，它定义了在允许值的范围内的最大值
      + 一种特殊情况：如果数据类型是周期性的（例如日期或时间），则的值`max`可能小于的值`min`，这表明范围可能会回绕；例如，它允许您指定从10 PM到4 AM的时间范围

    + maxlength

      + 有效期`text`，`search`，`url`，`tel`，`email`，和`password`，它定义字符的最大数目（作为UTF-16代码单位）的用户可输入到该字段。该值必须是整数值`0`或更高, 如果未`maxlength`指定no或指定了无效值，则该字段没有最大长度。此值还必须大于或等于的值`minlength`。

        如果输入到字段中的文本的长度大于UTF-16代码单元的长度，则输入将无法通过[约束验证](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Constraint_validation)`maxlength`。默认情况下，浏览器阻止用户输入的字符超过该`maxlength`属性所允许的字符。有关更多信息，请参见[客户端验证](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#client-side_validation)

    + min

      + 有效期`date`，`month`，`week`，`time`，`datetime-local`，`number`，和`range`，它定义了在允许值的范围的最负的值。如果[`value`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-value)输入的元素小于此值，则该元素将无法通过[约束验证](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Constraint_validation)。如果`min`属性的值不是数字，则元素没有最小值。

        该值必须小于或等于`max`属性的值。如果`min`属性存在但未指定或无效，则不会`min`应用任何值。如果`min`属性有效且非空值小于`min`属性允许的最小值，则约束验证将阻止表单提交。有关更多信息，请参见[客户端验证](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#client-side_validation)。

        有一种特殊情况：如果数据类型是周期性的（例如日期或时间），则的值`max`可能小于的值`min`，这表明范围可能会回绕；例如，它允许您指定从10 PM到4 AM的时间范围。

    + minlength

      + 有效期`text`，`search`，`url`，`tel`，`email`，和`password`，它定义的最小字符数目（UTF-16代码单位）的用户可输入到输入字段中。该值必须是小于或等于由所指定的值的非负整数值`maxlength`。如果未`minlength`指定no或指定了无效值，则输入没有最小长度。

        如果输入到字段中的文本的长度小于UTF-16代码单元的长度，则输入将无法通过[约束验证](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Constraint_validation)`minlength`，从而阻止表单提交。有关更多信息，请参见[客户端验证](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#client-side_validation)。

    + multiple

      + `multiple`如果设置了Boolean属性，则意味着用户可以在电子邮件小部件中输入逗号分隔的电子邮件地址，或者可以使用`file`输入选择多个文件。请参阅[电子邮件](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email)和[文件](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file)输入类型

    + name

      + 一个字符串，指定输入控件的名称
      + 如果未输入name或者为空时，输入的值不会跟随表单一起提交
      + 特殊情况
        + _charset_
          +  如果用做隐藏input类型元素的名称，在用户代理会自动将输入的内容设置为用于提交表单的字符编码
        + isindex
          + 历史原因[isindex](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fe-name)不允许使用该名称

    + pattern

      + 指定属性后，该属性是一个正则表单时，输入值value必须匹配正则表达式

    + placeholder

      + 为用户提供有关该字段中需要什么样的信息简短提示

    + readonly

      + 只读模式，指示用户不应编辑输入的值，属性支持`text`，`search`，`url`，`tel`，`email`，`date`，`month`，`week`，`time`，`datetime-local`，`number`，和`password`输入类型

    + required

      + 必填项，指示用户必须先输入一个值才提交拥有表单，属性被支承`text`，`search`，`url`，`tel`，`email`，`date`，`month`，`week`，`time`，`datetime-local`，`number`，`password`，`checkbox`，`radio`，和`file`的输入

    + size

      + 有效期为`email`，`password`，`tel`，和`text` `input`唯一的类型。指定显示多少输入
      + 值的实际单位取决于输入类型。对于`password`和`text`，它是许多字符（或`em`单位），其默认值是`20`，对于其他字符，它是`pixel`s。CSS宽度优先于size属性

    + src

      + `image`仅对输入按钮有效，`src`是字符串，指定要显示以表示图形提交按钮的图像文件的URL。请参阅[图像](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/image)输入类型

    + step

      + 对于数字输入类型（包括`number`，日期/时间输入类型和）有效`range`，该`step`属性是一个数字，用于指定值必须遵循的粒度。

      + 如果未明确包括在内：

        - `step`默认为1对`number`和`range`。
        - 对于日期/时间输入类型，`step`以秒表示， **默认步长为60秒**。步长比例因子为1000（如其他算法中所使用的，它将秒转换为毫秒）。

        该值必须是一个正数（整数或浮点数）或特殊值`any`，这意味着不隐含任何步进，并且允许任何值（除非其他约束，例如`min`和`max`）。

        如果`any`未显式设置，则`number`，日期/时间输入类型和`range`输入类型的`min`有效值等于步进的基础—步进值的值和增量，直到`max`指定的值为止

    + tabindex

      + 全局属性对所有元素（包括所有输入类型）均有效，一个整数属性，指示元素是否可以获取输入焦点（可聚焦），是否应该参与顺序键盘导航

    + title

      + 全局属性对所有元素（包括所有输入类型）均有效，该属性包含表示与该元素所属元素相关的咨询信息的文本

    + type

      + 指定要呈现的控件的类型
      + 值类型
        + text
        + password
        + email
        + date
        + number
        + file
        + checkbox
        + radio
        + button
        + color
        + datetime-local
        + hidden
        + image
        + month
        + range
        + submit
        + tel
        + url
        + week
        + 

    + width

      + `image`仅对输入按钮有效，`width`是显示以表示图形提交按钮的图像文件的宽度。请参阅[图像](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/image)输入类型。

    + value

      + 输入控件的值

+ [button](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button)

  + 定义
    + 一个可点击的按钮，用于提交[表单](https://developer.mozilla.org/en-US/docs/Learn/Forms)或任何地方访问，标准按钮功能的文件内
  + 属性
    + autofocus
      + 指定页面加载时按钮应具有输入[焦点](https://developer.mozilla.org/en-US/docs/Web/API/HTMLOrForeignElement/focus)， **文档中只有一个元素可以具有此属性**
    + autocomplete
      + 非标准且特定于Firefox的
    + disabled
      + 布尔值可防止用户与按钮交互：无法按下按钮或将其聚焦
    + form
      + 所述[form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)元件与（其按钮关联*形式所有者*）属性的值必须是`id`一个`<form>`相同的文件内
    + formaction
      + 处理提交按钮信息的URL。重写[`action`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form#attr-action)按钮的形式所有者的属性
    + formenctype
      + 如果按钮是一个提交按钮则指定如何对提交的表单数据进行编码,
      + 值类型
        + `application/x-www-form-urlencoded`：如果不使用该属性，则为默认值。
        + `multipart/form-data`：用于提交属性设置为的[``](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)元素。[`type`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-type)`file`
        + `text/plain`：指定为调试辅助；不应用于实际表单提交
    + formmethod
      + 如果该按钮是一个提交按钮则此属性指定用于提交表单的[HTTP方法](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
      + 值类型
        + post
          + 来自表单的数据在发送到服务器时包含在HTTP请求的主体中。在表单包含不应公开的信息（例如登录凭据）时使用
        + get
          + 表单数据以分隔符附加到表单的`action`URL `?`，然后将结果URL发送到服务器。当表单[没有副作用](https://developer.mozilla.org/en-US/docs/Glossary/Idempotent)（如搜索表单）时，请使用此方法
        + 
    + formnovalidate
      + 布尔属性指定在提交表单时不对其进行[验证](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
    + formtarget
      + 如果按钮是“提交”按钮，则此属性是作者定义的名称或标准的，带下划线前缀的关键字，指示在何处显示提交表单的响应
      + 值类型
        + _self
          + 加载到与当前浏览上下文相同的浏览器上下文中
        + _blank
          + 加载到新的未命名浏览上下文中
        + _parent
          + 加载到当前浏览器的父浏览器上下文中，如果没有父母行为与_self相同
        + _top
          + 加载到顶级浏览上下文中，如果没有父母行为与_self相同
    + name
      + 按钮名称
    + type
      + 按钮的默认行为
      + 值类型
        + button
          + 按钮没有默认行为，不执行任何操作
        + submit
          + 将表单数据提交到服务器
        + reset
          + 将所有控件重置为初始值
    + value
      + 定义`name`与表单数据一起提交时与按钮的关联的值

+ [textarea](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea)

  + 定义
    + 表示多行纯文本编辑控件
  + 属性
    + autocapitalize
      + iOS上的WebKit支持的非标准属性，
      + 值类型
        + `none`：完全禁用自动大写。
        + `sentences`：自动将句子的首字母大写。
        + `words`：自动大写单词的第一个字母。
        + `characters`：自动大写所有字符。
        + `on`：自iOS 5起不推荐使用。
        + `off`：自iOS 5起不推荐使用
    + autocomplete
      + 指示控件的值是否可以由浏览器自动完成
      + 值类型
        + off
          + 用户必须为每次使用在此字段中明确输入一个值，否则文档将提供自己的自动完成方法；浏览器不会自动完成输入
        + on
          + 浏览器可以根据用户在先前使用过程中输入的值自动完成该值
    + autocorrect
      + 指示在用户编辑时是否激活自动拼写校正和文本替换处理
      + 值类型
        + on
          + 启用自动拼写更正和文本替换
        + off
          + 禁用自动拼写更正和文本替换
        + 
    + autofocus
      + 布尔值，可以指定页面加载时表单控件应具有输入焦点。文档中只有一个与表单相关的元素可以指定此属性
    + cols
      + 文本控件的可见宽度，以平均字符宽度为单位。如果指定，则必须为正整数。如果未指定，则默认值为`20`
    + disabled
      + 布尔值，指示用户无法与控件进行交互
    + form
      + 元素所关联的表单元素（其“表单所有者”）。该属性的值必须是`id`同一文档中表单元素的
    + maxlength
      + 用户可以输入的最大字符数（UTF-16代码单元）
    + minlength
      + 用户应输入的最小字符数（UTF-16代码单元）
    + name
      + 控件的名称
    + placeholder
      + 用户提示可以在控件中输入的内容
    + readonly
      + 只读，不能输入，无法修改控件的值
    + required
      + 必填，在指定用户提交之前必须填写值
    + rows
      + 控制可见文本行数
    + spellcheck
      + 指定是否接受浏览器/os的拼写检查
      + 值类型
        + true
          + 表示该元素需要检查其拼写和语法
        + default
          + 元素将根据默认行为（可能基于父元素自己的`spellcheck`值）进行操作
        + false
          + 指示不应对元素进行拼写检查
    + wrap
      + 控件如何包装文本
      + 值类型
        + hard
          + 浏览器会自动插入换行符（CR + LF），以使每行的宽度不超过控件的宽度；该`cols`属性也必须指定才能生效
        + soft
          + 浏览器确保该值中的所有换行符均由CR + LF对组成，但不会插入任何其他换行符
        + off
          + `soft`但将外观更改为，`white-space: pre`这样超出`cols`的线段将不会被包裹，并且`<textarea>`变为水平滚动

+ [select](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select)

  + 定义
    + 提供选项菜单的控制
  + 属性
    + autocomplete
      + 一个[`DOMString`](https://developer.mozilla.org/en-US/docs/Web/API/DOMString)提供了一个提示[用户代理的](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)自动完成功能
    + autofocus
      + 布尔值，可以指定页面加载时表单控件应具有输入焦点。文档中只有一个表单元素可以具有该`autofocus`属性
    + disabled
      + 布尔值，指示用户无法与控件进行交互
    + form
      + 所述[form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)元件关联的`<select>`与（其*形式所有者*）
    + multiple
      + 布尔值，用户可以选多个选项，属性指示可以在列表中选择多个选项
    + name
      + 指定控件名称
    + required
      + 布尔值，指示必须选择具有非空字符串值的选项
    + size 
      + 控件为滚动列表框，则此属性表示列表中一次应可以见的行数
    + 

+ [option](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option)

  + 定义
    + 用于定义包含select或optgroup或datalist
  + 属性
    + disabled
      + 布尔值，此项不可选
    + label
      + 标签的文本，选项含义
    + selected
      + 初始选项
    + value
      + 选项值，值取自option元素的文本内容

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







