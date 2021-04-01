### Css

#### 选择器

##### 常规选择器

- 通配符选择器
  - 定义
    - 使用'*'号作为替代所有标签
- 元素选择器
  - 定义
    - 使用html元素作为选择器
- 类选择器
  - 定义
    - 使用'.'号为开头拼接有意义的字符串
- ID选择器
  - 定义
    - 使用'#'号为开头拼接有意义的字符串
- 父子选择器
  - 定义
    - 在标签选择器或class选择器或ID选择器中间使用'>'拼接，大于号前是父级选择器，大于号后是子类选择器
- 跨层级后代选择器
  - 定义
    - 在两个选择器之间使用空格拼接
- 相邻选择器
  - 定义
    - 在标签选择器或class选择器或ID选择器中间使用'+'拼接，加号前是兄选择器，加号后是弟选择器
- 普通兄弟选择器
  - 定义
    - 在标签选择器或class选择器或ID选择器中间使用'~'拼接，波浪号前是兄选择器，波浪号后是弟选择器
- 列组合选择器
  - 定义
    - '||'组合器选择属于某个表格行的节点
    - 使用比较少，通常使用类选择器或者ID选择器替代

##### 属性选择器

+ 过滤属性存在选择器
  + 定义
    + 使用中括号'[属性]'包括，过滤出元素上设置有该属性的元素
+ 过滤属性等于值选择器
  + 定义
    + 使用中括号'[属性=值]'包括，过滤出属性中等于设置的值的元素
+ 过滤前缀一选择器
  + 定义
    + 使用中括号'[属性|=值]'包括，过滤出为属性中包必须是完整且唯一的单词或者以中横杠'-'分隔开的元素
+ 过滤前缀二选择器
  + 定义
    + 使用中括号'[属性^=值]'包括，过滤出为属性中的前几个字母为值的元素
+ 过滤后缀选择器
  + 定义
    + 使用中括号'[属性$=值]'包括，过滤出为属性中包含的值的前缀的元素
+ 过滤属性包含值选择器
  + 定义
    + 使用中括号'[属性*=值]'包括，过滤出为属性中包含的值的元素

##### 伪类选择器

+ 链接未点击选择器
  + 定义
    + 使用':link'定义链接未点击时的元素
+ 链接已点击选择器
  + 定义
    + 使用':visited',过滤已经被点击过的链接元素
+ 链接按下未放开选择器
  + 定义
    + 使用':active',过滤鼠标按下未放开的元素
+ 滑过选择器
  + 定义
    + 使用':hover',过滤鼠标滑过时的元素
+ 排除选择器
  + 定义
    + 使用':not()'设置获取不符合条件的元素
+ 焦点选择器
  + 定义	
    + 使用':focus', 过滤当前获得焦点的元素
+ 匹配第一个子元素选择器
  + 定义
    + 使用':first-child'，匹配父元素的第一个子元素
+ 匹配最后一个子元素选择器
  + 定义
    + 使用':last-child',匹配父元素的最后一个子元素
+ 语言选择器
  + 定义
    + 使用':lang(c)'，匹配lang属性等于c的E元素
  + 使用上比较少
+ 表单激活选择器
  + 定义
    + 使用':enabled'，匹配表单中已被激活的元素
+ 禁用选择器
  + 定义
    + 使用':disabled', 匹配表单中已被禁用的元素
+ 选择框选择器
  + 定义	
    + 使用':checked'，匹配表单元素radio 或checkbox选择的元素
+ 下拉选择器
  + 定义
    + 使用':selection'，匹配表单下拉列表中选中的元素
+ 根元素选择器
  + 定义
    + 使用':root'，匹配根元素
+ 过滤N选择器
  + 定义
    + 使用':nth-child(n)'，匹配父元素的第n个元素
+ 过滤倒数N选择器
  + 定义
    + 使用':nth-last-child(n)', 匹配父元素倒数第n个元素
+ 过滤同种标签选择器
  + 定义
    + 使用':nth-of-type(n)'，仅匹配使用同一种标签的元素
+ 过滤倒数同种标签选择器
  + 定义
    + 使用':nth-last-of-type(n)', 仅匹配倒数使用同一种标签的元素
+ 第一个同种标签选择器
  + 定义
    + 使用':first-of-type',匹配父元素下的一个使用同种标签的元素
+ 最后一个同种标签选择器
  + 定义
    + 使用':last-of-type'，匹配父元素下最后一个使用同种标签的元素
+ Only选择器
  + 定义
    + 使用':only-child'，匹配父元素下仅有的一个子元素
+ Only同种标签选择器
  + 定义
    + 使用':only-of-type'，匹配父元素下仅有的一个同种标签元素
+ 空选择器
  + 定义
    + 使用':empty'，匹配一个不包含任何子元素的元素
+ target选择器
  + 定义
    + 使用':target', 匹配文档中特定"id"点击后的效果

##### 伪元素选择器

+ 元素的第一行选择器
  + 定义
    + 使用'::first-line'， 匹配元素的第一行
+ 元素的第一个字母选择器
  + 定义
    + 使用'::first-letter', 匹配元素的第一个字母
+ 元素前插入内容选择器
  + 定义
    + 使用'::before'，在元素之前插入生成的内容
+ 元素后插入内容选择器
  + 定义
    + 使用'::after'，在元素之后插入生成的内容

##### 选择器优先级

+ 引用优先级计算
  + 外部样式 ｜ 内部样式  <  内联样式
+ 声明样式优先级
  + 继承不如指定
  + !import > 内联 > ID > class|属性|伪类 > 元素选择器

##### [MDN伪类与伪元素](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements)

+ 在MDN上还有一部分为列举出来的选择器，比较少使用的

#### 样式

##### 布局样式

+ display

  + 定义

    + 改变元素的

  + 值类型

    + block

      + 将行内元素转换为块级元素

    + inline

      + 将块级元素转换为行内元素

    + inline-block

      + 元素保留块级元素的宽高度又有行内元素的特性，可以通过text-align设置对齐

    + inline-flex

      + 将元素转换为内联块级弹性伸缩显示

    + inline-table

      + 元素保留行内元素的特性体又有表格的特性

    + inherit

      + 从父元素上即成display的值

    + initial

      + 元素默认值，css官方定义（ie不支持）

    + unset

      + 当元素可以继承时为inherit，否则为默认值initial, 相当于不设置（ie不支持，safari9~不支持，ios9.2～不支持，Android4.4.4 ～不支持）

    + flex

      + 将元素转换为弹性盒子模型

    + table

      + 将元素转换为块级表格盒子模型

    + table-cell

      + 将元素转换为类似（td/th）一个表格单元格显示

    + table-column

      + 将元素转换为一个表格单元格列来显示

    + table-column-group

      + 将元素转换为类似（colgroup）一个或多个表格单元列分组显示

    + table-footer-group

      + 将元素转换为类似（tfoot）一个或多个行的分组显示

    + table-header-group

      + 将元素转换为类似（thead）一个或多个行的分组显示

    + table-row

      + 将元素转换为类似（tr）作为一个表格行显示

    + table-row-group

      + 将元素转换为类似（tr）一个或者多个表格行的分组显示

    + table-caption

      + 将元素转换为类似（caption）表格标题显示

    + none

      + 隐藏元素，不占用布局空间

    + grid

      + 指定容器为网格布局

    + inline-grid

      + 指定容器为行内元素，容器内采用网格布局

    + subgrid

      + 在网格元素中嵌套子网格元素，[详细参考](https://blogs.igalia.com/mrego/2016/02/12/subgrids-thinking-out-loud/)

    + contents

      + 将一个元素从边界框树型结构(box tree)中移去,

      + 迷之行为：

        + 在网上找了一个case，case中边框的设置被移除，没有显示

          ```html
          <div
                  style="display: contents; background: magenta; border:20px solid black; color: cyan; font: 30px/1 Monospace;">
                  <span style="background: black;">foobar</span> 
              </div>
          ```

          

    + list-item

      + 将不是列表元素的元素转换成类似列表的元素

      + 在chrome下没实现

        ```html
        <style>
          .div p {display: list-item;}
        </style>
        
        <div class="div">
             <p>list-item</p>
             <p>list-item</p>
             <p>list-item</p>
        </div>
        ```

        

    + flow

      + 处于一个试验形式的值，元素表现为内联框盒子或者块级框盒子，为内容建立新的块格式上下文（BFC）,或者是将内容集成到其父格式上下文中

    + flow-root

      + 将元素声明后都会变成块级元素，同时建立元素新的块级格式上下文(BFC)
      + 用来
        + 清除浮动
        + 去除margin合并现象
        + 实现两栏自适应布局

    + ruby

      + 实现元素旁注标记

    + ruby-base

      + 实现类似html元素rb

    + ruby-base-container

      + 实现类似html元素rbc

    + ruby-text

      + 实现类似html元素rt

    + ruby-text-container

      + 实现类似html元素rtc

+ flex

  + 定义
    + 设置盒模型的弹性宽度
  + 值类型
    + auto
      + 元素根据自身宽高来设置确定尺寸，会伸长并吸收flex容器的额外的自由空间，也会缩短自身宽高适应容器
    + initial
      + 元素根据自身宽高设置尺寸，会缩短自身以适应flex容器，不回伸长并吸收flex容器中额外的自由空间
    + none
      + 元素根据自身宽高来设置尺寸，非弹性盒子，不会缩短或伸长来适应flex容器
    + min-content
      + 采用内部元素最小宽度值最大的那个元素的宽度作为最终容器的宽度
    + inherit
      + 继承父元素设置
    + unset
      + 不设置

+ flex-basis

  + 定义
    + 设置在主轴方向上的初始大小
  + 值类型
    + auto
      + 参照元素的width 和height属性
    + fill
    + max-content
    + min-content
    + fit-content
    + cotnent
      + 基于flex元素的内容自动调整大小
    + inherit
      + 继承父元素设置的值
    + initial
      + 初始值
    + unset
    + none
      + 适用于不换行的内容固定或者较少的小控件元素上

+ flex-grow

  + 定义
    + 指定flex容器中剩余空间的分配（增长系数）计算方式，值为number，不允许负值
    + 分配方式
      + 
  + 值类型
    + inherit
      + 继承父级设置值
    + initial
      + 默认值
    + unset
      + 不设置

+ flex-shrink

  + 定义
    + 指定flex元素收缩规则，值为number，不允许负值
    + 值类型
      + inherit
        + 继承父级设置值
      + initial
        + 默认值
      + unset
        + 不设置

+ flex-direction

  + 定义
    + 确定主轴的排列方向
  + 值类型
    + row
      + 默认值，水平方向 从左向右排列
    + row-reverse
      + 水平方向，从右向左排列
    + column
      + 垂直方向，从上往下排列
    + column-reverse
      + 垂直方向，从下往上排列

+ flex-wrap

  + 定义
    + 定义子元素是否换行，如何换行
  + 值类型
    + nowarp
      + 默认值，不换行
    + wrap
      + 换行，第一行在上方
    + wrap-reverse
      + 换行，第一行在下方

+ flex-flow

  + 定义
    + flex-direction和flex-wrap的简写形式，输出"flex-flow: flex-direction || flex-wrap"
  + 值类型
    + row nowrap
      + 默认值

+ grid

  + 定义

    + 声明元素网格设置，值由以下细分样式拼接组成

  + 细分样式

    + grid-template

      + 定义
        + 设置网格中行、列与分区，由以下细分样式拼接
      + 值类型
        + none
          + 恢复默认值
      + 细分样式
        + grid-template-rows
          + 定义
            + 基于网格行的维度去定义网格线的名称和网格轨道的尺寸大小
          + 值类型
            + none
              + 表示不明确的网格，行和大小都有隐式指定
            + <length>
              + 非负值的长度大小
            + <percentage>
              + 非负值且相对于网格容器的百分比
            + <flex>
              + 非负值，使用fr单位来定义网格轨道大小的弹性系数
            + max-content
              + 一个用来表示以网格项的最大的内容来占据网格轨道的关键字
            + min-content
              + 一个用来表示以网格项的最大的最小内容来占据网格轨道的关键字
            + [minmax(min, max)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/minmax())
              + 定义大小范围的属性，大于等于min值，并且小于等于max值
              + 最大值可以设置为网格轨道系数值`<flex>` ，但最小值则不行
            + auto
              + 该网格轨道为最大时，该属性等同于 `<max-content>` ，为最小时，则等同于 `<min-content>`
            + [fit-content(<length> | <percentage>)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/fit-content)
              + 相当于公式 `min(max-content, max(auto, argument))`，类似于`auto` 的计算(即 `minmax(auto, max-content)`)，除了网格轨道大小值是确定下来的，否则该值都大于 `auto` 的最小值
            + [repeat(positive-integer | auto-fill | auto-fit | track-list)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/repeat())
              + 网格轨道的重复部分，以一种更简洁的方式去表示大量而且重复行的表达式
        + grid-template-columns
          + 定义
            + 基于网格列的维度去定义网格线的名称和网格轨道的尺寸大小
          + 值类型
            + none
              + 表示不明确的网格，列和大小都有隐式指定
            + <length>
              + 非负值的长度大小
            + <percentage>
              + 非负值且相对于网格容器的百分比
            + <flex>
              + 非负值，使用fr单位来定义网格轨道大小的弹性系数
            + max-content
              + 一个用来表示以网格项的最大的内容来占据网格轨道的关键字
            + min-content
              + 一个用来表示以网格项的最大的最小内容来占据网格轨道的关键字
            + [minmax(min, max)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/minmax())
              + 定义大小范围的属性，大于等于min值，并且小于等于max值
              + 最大值可以设置为网格轨道系数值`<flex>` ，但最小值则不行
            + auto
              + 该网格轨道为最大时，该属性等同于 `<max-content>` ，为最小时，则等同于 `<min-content>`
            + [fit-content(<length> | <percentage>)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/fit-content)
              + 相当于公式 `min(max-content, max(auto, argument))`，类似于`auto` 的计算(即 `minmax(auto, max-content)`)，除了网格轨道大小值是确定下来的，否则该值都大于 `auto` 的最小值
            + [repeat(positive-integer | auto-fill | auto-fit | track-list)](https://developer.mozilla.org/zh-CN/docs/Web/CSS/repeat())
              + 网格轨道的重复部分，以一种更简洁的方式去表示大量而且重复行的表达式
        + grid-template-areas
          + 定义
            + 网格区域grid areas在css中的特定名称
          + 值类型
            + none 
              + 网格容器没有定义任何的网格区块
            + <string>
              + 每一个给定的字符串会生成一行，一个字符串中用空格分隔的每一个单元(cell)会生成一列。多个同名的，跨越相邻行或列的单元称为网格区块(grid area)

    + grid-auto-rows

      + 定义
        + 指定隐式创建的行轨道大小，如果没有使用grid-template-rows指定大小，则使用隐式轨道
      + 值类型
        + <length>
          + 一个非负的长度
        + <percentage>
          + 相对于网格窗口块尺寸的非负值（百分比），如果网格容器尺寸不确定，则百分比值是auto
        + <flex>
          + 非负的、以 `fr` 为单位的维度指定轨道的弹性因子
        + max-content
          + 由网格元素中占用空间最大的那一个来决定轨道的尺寸
        + min-content
          + 由网格元素中占用空间最小的那一个来决定轨道的尺寸
        + minmax(min, max)
          + 一个不小于`min`且不大于`max`的尺寸范围
        + auto
          + 当用来指定最大值时与最大内容一致，当用来指定最小值时，它表示轨道中所有网格元素最小尺寸中的最大值（min-width/min-height指定）

    + grid-auto-columns

      + 定义
        + 隐式创建的网格纵向轨道的宽度
      + 值类型
        + <length>
          + 一个非负的宽度
        + <percentage>
          + 相对于网格窗口块尺寸的非负值（百分比），如果网格容器尺寸不确定，则百分比值是auto
        + <flex>
          + 非负的、以 `fr` 为单位的维度指定轨道的弹性因子
        + max-content
          + 由网格项的最大的内容来占据网格轨道
        + min-content
          + 由网格项的最小的内容来占据网格轨道
        + minmax(min, max)
          + 一个大于或等于 min 值，并且小于或等于 max 值的尺寸范围
        + fit-content(argument)
          + 相当于公式 `min(max-content, max(auto, argument))`
        + auto
          + 网格轨道为最大时，该属性等同于 `<max-content>` ，为最小时，则等同于 `<min-content>`

    + grid-auto-flow

      + 定义
        + 控制着自动布局算法怎样运作，精确指定在网格中被自动布局的元素怎样排列
      + 值类型
        + row
          + 指定自动布局算法按照通过逐行填充来排列元素，在必要时增加新行
        + column
          + 指定自动布局算法通过逐列填充来排列元素，在必要时增加新列
        + dense
          + 指定自动布局算法使用一种“稠密”堆积算法，如果后面出现了稍小的元素，则会试图去填充网格中前面留下的空白

    + grid-row

      + 定义

        + 网格单元与网格行（row）相关的尺寸和位置，可以通过在网格布局中的基线（line），跨度（span），或者什么也不做（自动），从而指定 [grid area](https://developer.mozilla.org/en-US/docs/Glossary/Grid_Areas) 的行起始与行结束

      + 值类型

        + auto 

          + 对网格的布置行为不做干涉，即自动布置，自动的 span 或者默认 span 值为 1

        + <custom-ident>

          + 存在自定义的基线名（'<custom-ident>-start'/'<custom-ident>-end'），它就将第一个这样的基线贡献给网格单元。

            **注意:** 被命名的网格区域（grid areas）会自动生成隐式的被命名的基线，因此指定 `grid-row: foo;` 将会选择这个命名区域的开始和结束的边界（除非在它之前存在显式指定的以 `foo-start`/`foo-end` 命名的其他基线）。

            否则，它就会被当作整数 `1` 与 `<custom-ident>` 一起指定

        + <integer> && <custom-ident>?

          + 第 n 条网格基线贡献给网格单元布置
          + 指定的是负数，则指的是从下边界向上边界计算的反向顺序
          + Integer 不能为0

        + span && [<integer> || <custom-ident>]

          + 为网格单元定义一个跨度，使得网格单元的网格区域中的一条边界远离另一条边界线 n 条基线。如果提供的是 <custom-ident>，则只有以此命名的基线才会被计算。如果网格线不足，则假定与搜索方向对应的显式网格一侧的所有隐式网格线都具有该名称。
          + integer默认设为1，值不能为0

      + 细分样式

        + grid-row-start(en-us)

          + 定义

            + 通过贡献一条线，一个跨度，或全无（自动）将其放置网格，从而指定其的直列起始沿指定网格行内的网格项的开始位置

          + 值类型

            + auto 

              + 对网格的布置行为不做干涉，即自动布置，自动的 span 或者默认 span 值为 1

            + <custom-ident>

              + 存在自定义的基线名（'<custom-ident>-start'/'<custom-ident>-end'），它就将第一个这样的基线贡献给网格单元。

                **注意:** 被命名的网格区域（grid areas）会自动生成隐式的被命名的基线，因此指定 `grid-row: foo;` 将会选择这个命名区域的开始和结束的边界（除非在它之前存在显式指定的以 `foo-start`/`foo-end` 命名的其他基线）。

                否则，它就会被当作整数 `1` 与 `<custom-ident>` 一起指定

            + <integer> && <custom-ident>?

              + 第 n 条网格基线贡献给网格单元布置
              + 指定的是负数，则指的是从下边界向上边界计算的反向顺序
              + Integer 不能为0

            + span && [<integer> || <custom-ident>]

              + 为网格单元定义一个跨度，使得网格单元的网格区域中的一条边界远离另一条边界线 n 条基线。如果提供的是 <custom-ident>，则只有以此命名的基线才会被计算。如果网格线不足，则假定与搜索方向对应的显式网格一侧的所有隐式网格线都具有该名称。
              + integer默认设为1，值不能为0

        + grid-row-end(en-us)

          + 定义

            + 通过贡献一条线，一个跨度，或全无（自动）将其放置网格，从而指定其的一字形端边缘指定网格行内的网格项的结束位置

          + 值类型

            + auto 

              + 对网格的布置行为不做干涉，即自动布置，自动的 span 或者默认 span 值为 1

            + <custom-ident>

              + 存在自定义的基线名（'<custom-ident>-start'/'<custom-ident>-end'），它就将第一个这样的基线贡献给网格单元。

                **注意:** 被命名的网格区域（grid areas）会自动生成隐式的被命名的基线，因此指定 `grid-row: foo;` 将会选择这个命名区域的开始和结束的边界（除非在它之前存在显式指定的以 `foo-start`/`foo-end` 命名的其他基线）。

                否则，它就会被当作整数 `1` 与 `<custom-ident>` 一起指定

            + <integer> && <custom-ident>?

              + 第 n 条网格基线贡献给网格单元布置
              + 指定的是负数，则指的是从下边界向上边界计算的反向顺序
              + Integer 不能为0

            + span && [<integer> || <custom-ident>]

              + 为网格单元定义一个跨度，使得网格单元的网格区域中的一条边界远离另一条边界线 n 条基线。如果提供的是 <custom-ident>，则只有以此命名的基线才会被计算。如果网格线不足，则假定与搜索方向对应的显式网格一侧的所有隐式网格线都具有该名称。
              + integer默认设为1，值不能为0

    + grid-column
      + 定义
        +  用于指定网格项目的大小和位置{ 通过为它的网格位置贡献线条，跨度或不添加任何内容（自动），从而指定其grid area
        + 是grid-column-start(en-us) 和 grid-column-end(en-us)的简写
      + 值类型
        + auto
          + 指示该属性对网格项目的放置没有任何作用，表示自动放置，自动跨度或默认跨度为1
        + <custom-ident>
          + 有一个名为"<custom-ident>-start"/"<custom-ident>-start"的命名行，则它将第一行添加到网格项目的位置，否则，将其视为与`<custom-ident>`一起指定了整数1
        + <integer> && <custom-ident>?
          + 将第n条网格线贡献到网格项目的位置。如果给定一个负整数，则从显式网格的末端开始，反向计数。
          + integer的值不能为0
        + span && [ <integer> || <custom-ident> ]
          + 将网格范围扩展到该网格项目的位置，以使该网格项目的网格区域的相应边缘距离相对边缘n行。
          + 如果省略<integer>，则默认为`1`。负整数或0无效。
      + 细分样式
        + grid-column-start(en-us)
          + 定义
            + 通过贡献线，跨度，或没有（自动）将其放置格指定网格列内的网格项目的起始位置
            + 起始位置定义了网格区域的块奇石边缘
          + 值类型
            + auto
              + 指示该属性对网格项目的放置没有任何作用，表示自动放置，自动跨度或默认跨度为1
            + <custom-ident>
              + 如果有一个名为name的命名行`<custom-ident>-start`，则它将第一行添加到网格项目的位置
              + **注意：**命名网格区域会自动生成这种形式的隐式命名线，因此，指定`grid-column-start: foo;`将选择该命名网格区域的起点（除非`foo-start`在其之前明确指定了另一条命名线）
              + 否则，将其视为`1`已与一起指定了整数`<custom-ident>`
            + <integer> && <custom-ident>?
              + 将第n条网格线贡献到网格项目的位置。如果给定一个负整数，则从显式网格的末端开始，反向计数。
              + integer的值不能为0
            + span && [ <integer> || <custom-ident> ]
              + 将网格范围扩展到该网格项目的位置，以使该网格项目的网格区域的相应边缘距离相对边缘n行。
              + 如果省略<integer>，则默认为`1`。负整数或0无效。
        + grid-column-end(en-us)
          + 定义
            + 通过贡献一条线，一个跨度，或全无（自动）将其放置网格，从而指定其的块尾端指定网格列内的网格项的结束位置
          + 值类型
            + auto
              + 指示该属性对网格项目的放置没有任何作用，表示自动放置，自动跨度或默认跨度为1
            + <custom-ident>
              + 如果有一个名为name的命名行`<custom-ident>-start`，则它将第一行添加到网格项目的位置
              + **注意：**命名网格区域会自动生成这种形式的隐式命名线，因此，指定`grid-column-start: foo;`将选择该命名网格区域的起点（除非`foo-start`在其之前明确指定了另一条命名线）
              + 否则，将其视为`1`已与一起指定了整数`<custom-ident>`
            + <integer> && <custom-ident>?
              + 将第n条网格线贡献到网格项目的位置。如果给定一个负整数，则从显式网格的末端开始，反向计数。
              + integer的值不能为0
            + span && [ <integer> || <custom-ident> ]
              + 将网格范围扩展到该网格项目的位置，以使该网格项目的网格区域的相应边缘距离相对边缘n行。
              + 如果省略<integer>，则默认为`1`。负整数或0无效
    + grid-area
      + 定义
        + 指定了一个内的网格项的大小和位置[网格](https://developer.mozilla.org/en-US/docs/Glossary/Grid)通过贡献一条线，一个跨度，或全无（自动）将其放置网格，从而指定其边缘网格区域
        + 是grid-row-start grid-column-start grid-row-end grid-column-end 四个的简写
      + 值类型
        + auto
          + 指示该属性对网格项目的放置没有任何作用，指示自动放置或默认跨度为`1`
        + <custom-ident>
          + 如果有一个名为' `<custom-ident>-start`'/' `<custom-ident>-end`'的命名行，则它将第一行添加到网格项目的位置
          + **注意：**命名网格区域会自动生成这种形式的隐式命名行，因此，指定`grid-area: foo;`将选择该命名网格区域的开始/结束边缘（除非在其之前显式指定了另一条名为`foo-start`/的行`foo-end`）
          + 否则，将其视为`1`已与一起指定了整数`<custom-ident>`
        + <integer> && <custom-ident>?
          + 将第n条网格线贡献到网格项目的位置。如果给定一个负整数，则从显式网格的末端开始，反向计数。
          + integer的值不能为0
        + span && [ <integer> || <custom-ident> ]
          + 将网格范围扩展到该网格项目的位置，以使该网格项目的网格区域的相应边缘距离相对边缘n行。
          + 如果省略<integer>，则默认为`1`。负整数或0无效

+ position

  + 定义
    + 将元素定位在某一个位置，配合left\right\top\bottom移动元素位置
  + 值类型
    + static
      + 默认值
    + relative
      + 相对定位，元素放置在未添加定位时的位置，
    + aboslute
      + 绝对定位，元素被移出正常文档流，根据最近非sticky定位的祖先的偏移来指定元素位置
    + fixed
      + 固定定位，根据屏幕视口的位置指定元素定位
    + sticky
      + 粘性定位，使用正常的布局行为

+ left

  + 定义
    + 指定定位元素左外边距与左边界之间的偏移，可以设置负值，正值向内偏移，负值向元素外偏移
    + 元素position值为static时，left属性无效
    + 当`position`设置为`sticky`时，如果元素在viewport里面，`left`属性的效果和position为`relative`等同；如果元素在viewport外面，`left`属性的效果和position为`fixed`等同
  + 当left 和 right属性同时存在时，根据容器排列方向取值，容器从左到右时取值left，反之取right
  + 值类型
    + auto
      + 对于绝对定位元素，元素将忽略此属性而以[`right`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/right)属性为准，如果此时设置`width: auto`，将基于内容需要的宽度设置宽度；如果`right`也为`auto`的话，元素的水平位置就是它假如作为静态(即static)元素时该在的位置。
      + 对于相对定位元素，元素相对正常位置的偏移量将基于[`right`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/right)属性；如果`right`也为`auto`的话，元素将不会有偏移
    + inherit
      + 值与父元素的计算值相同

+ right

  + 定义
    + 指定定位元素左外边距与左边界之间的偏移，可以设置负值，正值向内偏移，负值向元素外偏移
    + 元素position值为static时，right属性无效
    + 当`position`设置为`sticky`时，如果元素在viewport里面，`right`属性的效果和position为`relative`等同；如果元素在viewport外面，`right`属性的效果和position为`fixed`等同
  + 当left 和 right属性同时存在时，根据容器排列方向取值，容器从左到右时取值left，反之取right
  + 值类型
    + auto
      + 对于绝对定位元素，元素将忽略此属性而以[`left`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/left)属性为准，如果此时设置`width: auto`，将基于内容需要的宽度设置宽度；如果`left`也为`auto`的话，元素的水平位置就是它假如作为静态(即static)元素时该在的位置。
      + 对于相对定位元素，元素相对正常位置的偏移量将基于[`left`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/left)属性；如果`left`也为 `auto`的话，元素将不会有偏移。
    + inherit
      + 值与父元素的计算值相同

+ top

  + 定义
    + 定位元素的上外边距边界与其包含块上边界之间的偏移，非定位元素设置此属性
    + 当`position`设置为`absolute`或`fixed`时，`top`属性指定了定位元素上外边距边界与其包含块上边界之间的偏移。
    + 当`position`设置为`relative`时，`top`属性指定了元素的上边界离开其正常位置的偏移。
    + 当`position`设置为`sticky`时，如果元素在viewport里面，`top`属性的效果和position为`relative`等同；如果元素在viewport外面，`top`属性的效果和position为`fixed`等同。
    + 当`position`设置为`static`时，`top`属性无效
  + top与bottom同时指定时，并且height没有被指定或指定为auto时，top和bottom同时生效，height被限制时，top优先生效
  + 值类型
    + auto
    + inherit
      + 值与父元素的计算值相同

+ bottom

  + 定义
    + 定位元素下外边距边界与其包含块下边界之间的偏移，非定位元素设置此属性无效
    + 当`position`设置为`absolute`或`fixed`时，`bottom`属性指定了定位元素下外边距边界与其包含块下边界之间的偏移。
    + 当`position`设置为`relative`时，`bottom`属性指定了元素的下边界离开其正常位置的偏移。
    + 当`position`设置为`sticky`时，如果元素在viewport里面，`bottom`属性的效果和position为`relative`等同；如果元素在viewport外面，`bottom`属性的效果和position为`fixed`等同。
    + 当`position`设置为`static`时，`bottom`属性无效。
  + top与bottom同时指定时，并且height没有被指定或指定为auto时，top和bottom同时生效，height被限制时，top优先生效
  + 值类型
    + auto
      + 对于绝对定位元素，元素将忽略此属性而以[`top`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/top)属性为准，如果此时设置`height: auto`，将基于内容需要的高度设置宽度；如果`top`也为`auto`的话，元素的垂直位置就是它假如作为静态(即static)元素时该在的位置。
      + 对于相对定位元素，元素相对正常位置的偏移量将基于[`top`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/top)属性；如果`top`也为`auto`的话，元素将不会有偏移。
    + inherit
      + 计算结果的父级元素的值

+ float

  + 定义
    + 将元素浮动，允许文本和内联元素环绕它，脱离文档流
  + 值类型
    + none
      + 元素不进行浮动
    + left
      + 元素向左浮动
    + right
      + 元素向右浮动
    + inline-start
      + 元素必须浮动在其所在块容器的开始一侧，在ltr脚本中是左侧，在rtl脚本中是右侧
    + inline-end
      + 元素必须浮动在其所在块容器的结束一侧，在ltr脚本中是右侧，在rtl脚本中是左侧

+ margin

  + 定义
    + 设置块级元素上下左右的外边距，接受4个值
  + 值类型
    + auto
      + 使元素居中

+ margin-top

  + 定义
    + 设置元素顶部的外边距
  + 值类型
    + auto

+ margin-bottom

  + 定义
    + 设置元素底部的外边距
  + 值类型
    + auto

+ margin-left

  + 定义
    + 设置元素左边的外边距
  + 值类型
    + auto

+ margin-right

  + 定义
    + 设置元素右边的外边距
  + 值类型
    + auto

+ padding

  + 定义
    + 元素四条边的内间距区域

+ padding-top

  + 定义
    + 元素内顶部的内间距

+ padding-bottom

  + 定义
    + 元素内底部的内间距

+ padding-left

  + 定义
    + 元素内左边的内间距

+ padding-right

  + 定义
    + 元素内右边的内间距

+ width

  + 定义
    + 设置元素宽度，元素设置了min-width或者max-width,这两者属性的优先级高于width
  + 值类型
    + auto
      + 浏览器将会为指定的元素计算并选择一个宽度
    + max-content
      + 元素内容固有的（intrinsic）合适宽度
    + min-content
      + 元素内容固有的最小宽度
    + fit-content
      + 取以下两种值中的较大值:
        - 固有的最小宽度
        - 固有首选宽度（max-content）和可用宽度（available）两者中的较小值

+ height

  + 定义
    + 指定元素的高度，
  + 值类型
    + <length>
      + 设置一个绝对值
    + <percentage>
      + 将高度定义为相对包含块高度的百分比
    + border-box
      + 如果设置该值，则length或者percentage会设置为该元素的border-box
    + content-box
      + 如果设置该值，则length或者percentage会设置为该元素的content-box
    + auto
      + 由浏览器为元素计算并选择一个高度
    + fill
      + 根据文字方向，使用fill-available作为行大小或者块大小
    + max-content
      + 设置为允许的最大高度
    + min-content
      + 设置为允许的最小高度
    + fit-content
      + 将fill-content公式中的可用位置替换为特定的参数进行使用，如min(max-content,max(min-content))

+ box-sizing

  + 定义
    + 定义user agent应该如何计算一个元素的总宽度和总高度
  + 值类型
    + border-box
      + 将标准盒子改变成ie盒子，width和height包内容、内边距和边框
    + content-box
      + 默认值，标准盒子模型计算方式，width和height只包含内容的宽和高

+ max-width

  + 定义
    + 给元素设置最大宽度值
  + 值类型
    + none
      + 未设置最大值
    + <length>
      + 设置绝对值为宽度
    + <percentage>
      + 以父级容器的宽度百分比为最大宽度
    + max-content
      + 固有的首选宽度，根据内容的宽度设置最大宽度值
    + min-content
      + 固有最小宽度, 根据内容最小换行计算出宽度，英文以一个单词的长度计算宽度，中文按一个文字计算宽度
    + fill-available
      + 包含的块宽度减去水平边距，边框和填充
    + fit-content
      + 与max-content等价, 根据内容的宽度设置最大宽度值

+ min-width

  + 定义
    + 给定元素设置最小宽度，min-width会覆盖max-width和width
  + 值类型
    + <length>
      + 固定的最小宽度，值为绝对值
    + <percentage>
      + 固定的最小宽度，值为父级容器的百分比宽度
    + auto
      + 用于弹性元素的默认最小宽度
    + max-content
      + 固有首选宽度，根据内容的宽度设置最大宽度值
    + min-content
      + 固有最小宽度，根据内容最小换行计算出宽度，英文以一个单词的长度计算宽度，中文按一个文字计算宽度
    + fill-available
      + 包含块的宽度减去水平margin、border和padding
    + fit-content
      + 等同于 min(max-content, max(min-content, fill-available)

+ max-height

  + 定义
    + 设置元素的最大高度
    + max-height 会覆盖height, 而min-height 会覆盖 max-height
  + 值类型
    + <length>
      + 为绝对值
    + <percentage>
      + 为父级容器高度的百分比
    + auto
      + 浏览器将计算并max-height为指定的元素选择a
    + none
      + 盒子的大小没有限制
    + max-content
      + 固定首选max-height
    + min-content
      + 固定首选max-height
    + fit-content
      + 使用fit-content公式，将可用空间替换为指定的参数，即。min(max-content, max(min-content, argument))

+ min-height

  + 定义
    + 设置元素的最小高度
    + 当 min-height 大于 max-height 或 height 时，元素的高度会设置为 min-height 的值
  + 值类型
    + <length>
      + 为绝对值
    + <percentage>
      + 为父级容器高度的百分比
    + auto
      + 浏览器将计算并max-height为指定的元素选择a
    + none
      + 盒子的大小没有限制
    + max-content
      + 固定首选min-height
    + min-content
      + 固定首选min-height
    + fit-content
      + 使用fit-content公式，将可用空间替换为指定的参数，即。min(max-content, max(min-content, argument))

+ overflow

  + 定义
    + 定义一个元素的内容他打而无法适应块级格式化上下文，
  + 值类型
    + hidden
      + 子元素宽高度大于父级元素宽高度时子元素被裁剪去超出的宽高度，不提供滚动条
    + visible
      + 默认值，不裁剪，宽度超出父级
    + scroll
      + 内容父级容器包含超出宽高度，显示滚动条，拖拽滚动条显示其他内容
    + auto
      + 取决子元素内容，如果超出父级容器则显示滚动条，不超出则不显示滚动条
    + overlay
      + 与auto类似，但是滚动条在内容之上，不占用容器空间，仅基于webkit和blink的浏览器支持

+ overflow-x

  + 定义
    + 块级元素内容在水平方向上发生溢出时，如何处理截断溢出内容或者显示滚动条或者显示溢出内容
  + 值类型
    + hidden
      + 子元素宽高度大于父级元素宽高度时子元素被裁剪去超出的宽高度，不提供滚动条
    + visible
      + 默认值，不裁剪，宽度超出父级
    + scroll
      + 内容父级容器包含超出宽高度，显示滚动条，拖拽滚动条显示其他内容
    + auto
      + 取决子元素内容，如果超出父级容器则显示滚动条，不超出则不显示滚动条

+ overflow-y

  + 定义
    + 块级元素内容在垂直方向上发生溢出时，如何处理截断溢出内容或者显示滚动条或者显示溢出内容
  + 值类型
    + hidden
      + 子元素宽高度大于父级元素宽高度时子元素被裁剪去超出的宽高度，不提供滚动条
    + visible
      + 默认值，不裁剪，宽度超出父级
    + scroll
      + 内容父级容器包含超出宽高度，显示滚动条，拖拽滚动条显示其他内容
    + auto
      + 取决子元素内容，如果超出父级容器则显示滚动条，不超出则不显示滚动条

+ z-index

  + 定义
    + 设定一个元素的层级位置，值越大覆盖值较小的元素
  + 值类型
    + auto
      + 盒子不会创建新的本地堆叠上下文，
    + <integer>
      + 生成盒子在当前堆叠上下文中的堆叠层级，值越大层级越高

+ text-align

  + 定义
    + 设置行内内容如何相对于父级元素的对齐
  + 值类型
    + left
      + 行内内容向左对齐
    + right
      + 行内内容向右对齐
    + center
      + 行内内容居中
    + justify
      + 文字向两侧对齐，文本中最后一行无效
    + justify-all
      + 文字向两侧对齐，强制文本中最后一行向两侧对齐
    + start
      + 如果内容方向是左至右，则等于left，反之则为right
    + end
      + 如果内容方向是左至右，则等于right，反之则为left
    + match-parent
      + 区别在于start和end的值根据父元素的direction确定，并被替换为恰当的left或right

+ vertical-align

  + 定义
    + 指定行内元素（inline）或者表格单元格元素(table-cell)的垂直对齐方式
  + 值类型
    + <length>
      + 使元素的基线对齐到父元素的基线之上的给定长度，可以是负数
    + <percentage>
      + 使元素的基线对齐到父元素的基线之上给定的百分比
    + top
      + 使元素及其后代元素的顶部与整行的顶部对齐
    + bottom
      + 是元素及其后代元素的底部与整行的底部对齐
    + middle
      + 使元素的中部与父元素的基线加上父元素x-height的一半对齐
    + super
      + 使元素的基线与父元素的上标基线对齐
    + baseline
      + 元素的基线与父元素的基线对齐
    + sub
      + 元素的基线与父
    + text-top
      + 使元素的顶部与父元素的字体顶部对齐
    + text-bottom
      + 使元素的地步与父元素的字体底部对齐

+ align-items

  + 定义
    + 将所有直接子节点上的align-self值设置为一个组
  + 值类型
    + normal
      + 取决于我们处在什么布局模式中
        + 在绝对定位的布局中，对于被替代的绝对定位盒子，这个效果和`start?`的效果的一样；对于其他所有绝对定位的盒子，这个效果和`stretch`的效果一样。 
        + 在绝对定位布局的静态位置上，效果和`stretch`一样。
        + 对于那些弹性项目而言，效果和`stretch`一样。
        + 对于那些网格项目而言，效果和`stretch`一样，除了有部分比例或者一个固定大小的盒子的效果像`start`。
        + 这个属性不适用于会计盒子和表格
    + stretch
      + 弹性元素被在侧轴方向被拉伸到与容器相同的高度或宽度
    + start
      + 物品在适当的轴线上朝着对齐容器的起始边缘彼此齐平包装
    + end
      + 物品在适当的轴线上朝着对齐容器的末端彼此齐平包装
    + left
      + 物品朝对齐容器的左边缘彼此齐平包装
    + center
      + 如果元素在侧轴居中。如果元素在侧轴居中。那么在两个方向上重叠距离相同
    + right
      + 物品在适当的轴线上朝着对齐容器的右边缘彼此齐平地包装
    + flex-start
      + 元素向侧轴起点对齐
    + flex-end
      + 元素向侧轴终点对齐
    + self-start
      + 物品在适当的轴线上齐平包装到物品起始侧的对齐容器的边缘
    + self-end
      + 物品在适当的轴线上齐平包装到物品端面的对齐容器的边缘
    + baseline
      + 所有元素向垂直对齐。侧轴起点到元素距离最大的元素将会在侧轴起点对齐对齐
    + first baseline
      + 所有元素向垂直对齐。侧轴起点到元素距离最大的元素将会在侧轴起点对齐对齐
    + last baseline
      + 所有元素向垂直对齐。侧轴起点到元素距离最大的元素将会在侧轴起点对齐对齐
    + safe
      + 与alignment关键字一起使用。如果选择的关键字表示项目溢出对齐容器而导致数据丢失，则将对齐该项目，就好像对齐方式是 `start`
    + unsafe
      + 与alignment关键字一起使用。无论项目和对齐容器的相对大小如何，是否可能发生导致数据丢失的溢出，都应遵守给定的对齐值

+ justify-content

  + 定义
    + 浏览器之间如何分配顺着弹性容器主轴的元素之间及其周后的空间
  + 值类型
    + center
      + 伸缩元素向每行中点排列。每行第一个元素到行首的距离将与每行最后一个元素到行尾的距离相同
    + start
      + 从行首开始排列。每行第一个元素与行首对齐，同时所有后续的元素与前一个对齐
    + end
    + flex-start
      + 从行首开始排列。每行第一个弹性元素与行首对齐，同时所有后续的弹性元素与前一个对齐
    + flex-end
      + 从行尾开始排列。每行最后一个弹性元素与行尾对齐，其他元素将与后一个对齐
    + left
      + 伸缩元素一个挨一个在对齐容器得左边缘，如果属性的轴与内联轴不平行，则`left`的行为类似于`start`
    + right
      + 元素以容器右边缘为基准，一个挨着一个对齐,如果属性轴与内联轴不平行，则`right`的行为类似于`end`
    + baseline / first baseline / last baseline
      + 指定参与第一个或最后一个基线对齐方式：将框的第一个或最后一个基线集的对齐基线与其基线共享组中所有框的共享的第一个或最后一个基线集中的对应基线对齐
      + 回退定位 `first baseline` 是 `start`，一只为 `last baseline` 是 `end`
    + space-between
      + 在每行上均匀分配弹性元素。相邻元素间距离相同。每行第一个元素与行首对齐，每行最后一个元素与行尾对齐
    + space-around
      + 在每行上均匀分配弹性元素。相邻元素间距离相同。每行第一个元素到行首的距离和每行最后一个元素到行尾的距离将会是相邻元素之间距离的一半
    + space-evenly
      + flex项都初始同轴均匀分布在指定的分隔容器中。相邻的flex项之间的间距，初始起始位置到第一个flex项的间距，主轴结束位置到最后一个flex项的间距，都完全一样
    + stretch
      + 如果项目的组合大小小于对齐容器的大小，则任何 `auto`大小的项目都将其大小均等地（不成比例地）增加，同时仍要遵守[`max-height`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/max-height)/ [`max-width`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/max-width)（或等效功能）所施加的约束，因此，合并后的大小沿主轴精确地填充对齐容器
    + safe
      + 与对齐关键字一起使用，如果扩展的关键字会导致元素重叠容器造成数据丢失，那么将会使用 `start` 代替它
    + unsafe
      + 无论项目和对齐容器的相对大小如何，都应遵守给定的对齐值

##### 修饰样式

+ border
  + 定义
    + 设置元素的边框,值中包含边框宽度、边框样式、边框颜色
  + 细分样式
    + border-top
      + 定义
        + 设置元素的顶部边框,值中包含边框宽度、边框样式、边框颜色
    + border-bottom
      + 定义
        + 设置元素的底部边框,值中包含边框宽度、边框样式、边框颜色
    + broder-left
      + 定义
        + 设置元素的左边边框,值中包含边框宽度、边框样式、边框颜色
    + border-right
      + 定义
        + 设置元素的右边边框,值中包含边框宽度、边框样式、边框颜色
+ border-style
  + 定义
    + 设置所有边框的样式
  + 边框样式
    + none
      + 不显示边框
    + hidden
      + 不现实边框
    + dotted
      + 圆点边框
    + dashed
      + 虚线边框
    + solid
      + 实现边框
    + dobule
      + 双实现边框
    + groove
      + 雕刻效果边框
    + ridge
      + 浮雕效果边框
    + inset
      + 陷入效果边框
    + outset
      + 突出效果的边框
  + 细分样式
    + 
+ border-width
  + 定义
    + 设置元素的边框宽度
  + 值类型
    + <length>
      + 绝对值，单位px
    + thin
      + 细边线
    + medium
      + 中等边线
    + thick
      + 宽边线
  + 细分样式
    + border-top-width
    + border-left-width
    + border-right-width
    + border-bottom-width
+ border-color
  + 定义
    + 设置边框颜色配置，值为颜色英文名称或者以#号拼接十六进制的色值
  + 细分样式
    + border-top-color
    + border-left-color
    + border-right-color
    + border-bottom-color
+ border-radius
  + 定义
    + 设置外边框圆角
  + 细分样式
    + border-top-left-radius
    + border-top-right-radius
    + border-bottom-left-radius
    + border-bottom-right-radius
+ text-shadow
  + 定义
    + 设置文本阴影,阴影值由元素在X和Y方向的偏移量、模糊半径和颜色值组成
    + 值的组成
      + <color>
        + 设置值为颜色英文名称或者以#拼接的十六进制颜色，如果没有设置则由user agent自动选择颜色
      + <offset-x> <offset-y>
        + 设置阴影相对文字的偏移量，x指水平偏移量，y指垂直偏移量
      + <blur-radius>
        + 默认为0，值越大，模糊半径越大，阴影也越大越淡
+ box-shadow
  + 定义
    + 设置元素的边框外阴影效果，值包括阴影的X轴偏移量、Y轴偏移量、模糊半径、扩散半径和颜色
    + 值的组成
      + inset	
        + 默认阴影在边框外，指定值阴影在边框内
      + <offset-x> <offset-y>
        + 设置阴影相对元素边框外的偏移量，x指水平偏移量，x为正值位于右边负值位于左边，y指垂直偏移量，y为正值位于下方负值位于上方
      + <blur-radius>
        + 值越大，模糊面积越大，阴影就越大越淡。 不能为负值， 默认为0。
          + 计算对于长而直的阴影边缘，它会创建一个过渡颜色用于模糊 以阴影边缘为中心、模糊半径为半径的局域，过渡颜色的范围在完整的阴影颜色到它最外面的终点的透明之间
      + <spread-radius>
        + 取正值时，阴影扩大；取负值时，阴影收缩。默认为0
      + <color>
        + 值为颜色英文单词或者以#号拼接十六进制色值，默认由user agent指定，safari 取透明
+ backgroud
  + 定义
    + 设置元素背景，值为背景图像的位置+背景图像+背景定位+背景尺寸+是否重复组成
  + 细分样式
    + background-color
      + 定义
        + 设置元素的背景颜色，值为英文颜色单词或者以#号拼接十六进制的色值，透明色transparent也是一种颜色
    + background-image
      + 定义
        + 为元素设置一个或多个背景图像
      + 值类型
        + none
          + 无背景关键字
        + <image>
          + 标记显示的图片，支持多背景设置，以逗号分隔开
    + background-position
      + 定义
        + 为背景设置一个初始位置
      +  值类型
        + <length>
          + 绝对值（x, y）
        + <percentage>
          + 为元素的百分比（x, y）
        + top
          + 用来指定背景放在元素顶部边缘
        + bottom
          + 用来指定背景放在元素底部边缘
        + left 
          + 用来指定背景放在元素左边边缘
        + right
          + 用来指定背景放在元素右边边缘
        + center
          + 用来指定背景居中
      + 如果一个值是 `top` 或 `bottom`，那么另一个值不应该是 `top` 或 `bottom`
      + 如果一个值是 `left` 或  `right`，那么另一个值不应该是 `left` 或 `right` 
    + background-repeat
      + 定义
        + 设置背景图片重复的方式，背景图像可以沿着水平轴、垂直轴、两个轴重复或者根本不重复
      + 值类型
        + no-repeat
          + 不重复
        + repeat-x
          + x轴重复
        + repeat-y
          + y轴重复
        + repeat
          + x、y轴都重复
        + space
          + 重复，不会裁剪
          + **图像会尽可能得重复, 但是不会裁剪. 第一个和最后一个图像会被固定在元素(element)的相应的边上, 同时空白会均匀地分布在图像之间. [`background-position`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-position)属性会被忽视, 除非只有一个图像能被无裁剪地显示. 只在一种情况下裁剪会发生, 那就是图像太大了以至于没有足够的空间来完整显示一个图像.**
        + round
          + **随着允许的空间在尺寸上的增长, 被重复的图像将会伸展(没有空隙), 直到有足够的空间来添加一个图像. 当下一个图像被添加后, 所有的当前的图像会被压缩来腾出空间. 例如, 一个图像原始大小是260px, 重复三次之后, 可能会被伸展到300px, 直到另一个图像被加进来. 这样他们就可能被压缩到225px.**
          + 
    + background-clip
      + 定义
        + 设置元素的背景（背景图片或颜色）是否延伸到边框、内边距盒子、内容盒子下面
      + 值类型
        + border-box
          + 背景延伸至边框外沿（但是在边框下层）
        + padding-box
          + 背景延伸至内边距外沿，不会绘制到边框处
        + content-box
          + 背景被裁剪至内容区外沿
        + text
          + 背景被裁剪成文字的前景色
    + background-size
      + 定义
        + 设置背景图片的大小，图片可以保有其原有的尺寸，或者拉伸到新的尺寸，或者在保持其原有比例的同时缩放到元素的可用空间的尺寸
      + 值类型
        + <length>
          + 指定背景图片大小，不能为负值
        + <percentage>
          + 指定背景图片相对背景区（background positioning area）的百分比。背景区由[`background-origin`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-origin)设置，默认为盒模型的内容区与内边距，也可设置为只有内容区，或者还包括边框。如果[`attachment`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-attachment) 为`fixed`，背景区为浏览器可视区（即视口），不包括滚动条。不能为负值。
        + auto
          + 以背景图片的比例缩放背景图片
        + cover
          + 缩放背景图片以完全覆盖背景区，可能背景图片部分看不见
        + contain
          + 缩放背景图片以完全装入背景区，可能背景区部分空白
    + backgrounr-attachment
      + 指定背景图片在可视区域的位置
      + 值类型
        + fixed
          + 背景相对于视口固定，不随滚动条滚动
        + local
          + 背景相对于元素的内容固定，会随着滚动条滚动
        + scroll
          + 背景相对于元素本身固定， 而不是随着它的内容滚动（对元素边框是有效的）
+ font
  + 定义
    + 指定文本字体,值设置时必须包含font-size和font-family,其余属性可选
  + 值类型
    + caption
      + 用于标题控件的系统字体
    + icon
      + 用于标签图标的系统字体
    + menu
      + 菜单中使用的系统字体
    + message-box
      + 用于对话框的系统字体
    + small-caption
      + 用于小标题控件的系统字体
    + status-bar
      + 用于窗口状态栏的系统字体
    + <font-style>...
      + 值设定依据细分样式
  + 细分样式
    + font-style
      + 定义
        + 允许选择font-family字体下的italic或oblique样式
      + 值类型
        + normal
          + 常规字体
        + italic
          + 选择斜体，如果当前字体没有可用的斜体版本，会选用倾斜体（`oblique` ）替代
        + oblique
          + 选择倾斜体，如果当前字体没有可用的倾斜体版本，会选用斜体（`italic` ）替代，则选择与指定角度最接近的一个斜，则浏览器将通过将正常的面倾斜指定的数量来合成字体的倾斜版本。有效值为度值`-90deg`到的`90deg`含（包括）值（css4 草案）
          + 
    + font-variant
      + 定义
        + 字体变形
      + 值类型
        + normal
          + 规定一个常规字型
        + none
          + 将font-veriant-ligatures为none,其他简写属性的值设定为normal
      + 细分样式
        + font-variant-caps
          + 定义
            + 控制大写字母特殊字符的使用
          + 值类型
            + normal
              + 关闭一切特殊字符变体的使用
            + small-caps
              + 允许小型大写字母的使用，小型大写字母指使用大写形式，尺寸对应小写字母相同的字母
            + all-small-caps
              + 将大小写字母全部转换为小型大写字母
            + petite-caps
              + 允许特小型大写字母的使用
            + all-petite-caps
              + 将大小写字母全部转换为大写字母
            + unicase
              + 允许将大写字母转化为小型大写字母与普通小写字母的混用
            + titling-caps
              + 允许首字母大写
        + font-variant-numeric
          + 定义
            + 控制数字，分数和序号标记的替代字形的使用
          + 值类型
            + normal
              + 特性均不启用
            + ordinal
              + 启用序数形式启用
            + slashed-zero
              + 启用区分零显示，强制使用带有斜杠的0
            + lining-nums
              + 启用内衬数字显示，使数字全部对齐到基线
            + tabular-nums
              + 启用表格数字显示，使数字等宽，易于像表格对齐
            + oldstyle-nums
              + 启用旧式数字显示，部分数字下沉
            + proportional-nums
              + 启用比例数字显示，使数字变成基于字形体本身形状的特定宽度表现
            + diagonal-fractions
              + 启用斜角分数显示，使分子和分母变成像下标字，并用变长的斜线分隔
            + stacked-fractions
              + 启用标准分数显示。使分子在上，分母在下，并用水平线分隔
        + font-variant-alternates
          + 定义
            + 控制备用字体的使用
          + 值类型
            + normal
              + 禁用备用字体
            + historical-forms
              + 启用历史类型-过去常见但今天不常见的字体
            + stylistic()
              + 函数可以为个别字体启用字体样式替换
            + styleset()
              + 函数可以对字符集启用字体样式替换
            + character-variant()
              + 数启用字符的特定样式替代
            + swash()
              + 启用斜字体
            + ornaments()
              + 启用装饰物
            + annotation()
              + 支持注释, 如带圆圈的数字或倒置的字符
        + font-variant-ligatures
          + 定义
            + 控制着其所应用元素文本的 [连字](https://developer.mozilla.org/en-US/docs/Glossary/Ligature)与 [上下文形式](https://developer.mozilla.org/en-US/docs/Glossary/contextual_forms)
          + 值类型
            + normal
              + 默认值，在渲染时会使用常用的连字，连字的效果取决于字体，语言和脚本
            + none
              + 不使用任何连字，包括常规的形式
            + no-common-ligatures
              + 停用最常见的连字
            + common-ligatures
              + 激活最常见的连字
            + no-discretionary-ligatures
              + 禁用特定的连字
            + discretionary-ligatures
              + 激活特定的连字
            + historical-ligatures
              + 激活旧书中历史上使用的连字
            + no-historical-ligatures
              + 禁用旧书中历史上使用的连字
            + contextural
              + 指定要字母适应上下文替代项
            + no-contextural
              + 防止字母适应上线使用
        + font-variant-east-asian
          + 定义
            + 控制使用东亚脚本替代字形，像日本和中国的
          + 值类型
            + normal
              + 停用此类备用字形的使用
            + ruby
              + 强制将特殊字形用于ruby字符
            + jis78
              + 显示的逻辑字形变体
            + jis83
              + 显示的逻辑字形变体
            + jis90
              + 显示的逻辑字形变体
            + jis04
              + 显示的逻辑字形变体
            + simplified
              + 使用简体中文字形
            + traditional
              + 使用繁体中文字形
            + proportional-width
              + 激活宽度不同的东亚字符集
            + full-witdh
              + 激活所有相同的，大致为正方形的宽度度量的东亚字符集
    + font-weight
      + 定义
        + 字体的粗细程度
      + 值类型
        + normal
          + 正常粗细
        + bold
          + 加粗
        + lighter
          + 比从父元素继承来的值更细(处在字体可行的粗细值范围内)
        + bolder
          + 比从父元素继承来的值更粗 (处在字体可行的粗细值范围内)
        + <number>
          + 介于1到1000之间的数值
    + font-size
      + 定义
        + 指定字体的大小
      + 值类型
        + <length>
          + 正数
        + <percentage>
          + 父元素字体大小的正数,百分比
        + xx-small / x-small / small / medium / large / x-large / xx-large
          + 绝对大小关键字定义相对于用户的默认字体大小
        + larger / smaller
          + 比父元素的字体大或小，使用与上面的关键字的相近缩放比率
    + font-family
      + 定义
        + 允许您通过给定一个有先后顺序的，由字体名或者字体族名组成的列表来为选定的元素设置字体
      + 值类型
        + <family-name>
          + 字体族的名称
        + <generic-name>
          + 通用字体族名， 用于在指定的字体不可用时给出较好的字体
    + font-stretch
      + 定义
        + 字体定义一个正常或经过伸缩变形的字体外观,当有多种字体可供选择时，会为字体选择最适合的大小
      + 值类型
        + normal
          + 指定默认字体
        + semi-condensed, condensed, extra-condensed, ultra-condensed
          + 小于默认字体，其中ultra-condensed是缩的最小的字体
        + semi-expanded, expanded, extra-expanded, ultra-expanded
          + 大于默认字体的值
      + 细分样式
        + font-feature-settings
          + 定义
            + 用于控制OpenType字体中的高级印刷功能
          + 值类型
            + normal
              + 文本使用默认设置进行布局
            + <feature-tag-value>
              + 在呈现文本时，OpenType要素标记值的列表被传递到文本布局引擎以启用或禁用字体特征
    + font-size-adjust
      + 定义
        + 字体大小应取决于小写字母，而不是大写字母
      + 值类型
        + normal 
          + 依据font-size属性决定大小
        + <number>
          + 根据使用小写字母大小为该值乘以font-size的结果定义习题大小
    + font-kerning
      + 定义
        + 设置是否使用字体中储存的字距信息
      + 值类型
        + auto
          + 浏览器来决定是否使用字体字距
        + normal
          + 必须应用字体中的字距信息
        + none
          + 禁用字体中的字距信息
+ line-height
  + 定义
    + 设置文本的间距
  + 值类型
    + normal
      + 取决于元素的font-family
    + <number>
      + 无单位数字乘以元素的字体大小
    + <length>
      + 指定用于计算line-box的高度
    + <percentage>
      + 与元素自身的字体大小有关，值为百分比
    + -moz-block-height
      + 将行高设置为当前块的内容区域高度
+ letter-spacing
  + 定义
    + 设置文本字符的间距表现
  + 值类型
    + normal
      + 间距按照当前字体的正常间距确定的
    + <length>
      + 指定文字间的间距以替代默认间距

##### 动画样式

+ transform
+ animation

##### 规则样式

+ @import
+ @font-face
+ @charset
+ @keyframes
+ @namespaces
+ @media
+ @page





