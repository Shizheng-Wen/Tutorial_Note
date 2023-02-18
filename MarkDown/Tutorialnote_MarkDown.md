# MarkDown基本用法

---

## 标题

* 输入

  ```markdown
  # 一级标题
  ## 二级标题
  ### 三级标题
  #### 四级标题
  ##### 五级标题
  ###### 六级标题
  ```

* 输出

  # 一级标题

  ## 二级标题

  ### 三级标题

  #### 四级标题

  ##### 五级标题

  ###### 六级标题



## 引用

* 输入

  ```markdown
  > 引用文字
  ```

* 输出

  > 引用文字



## 列表

1. 无序列表

   * 输入

     ```markdown
     * 样式一
     + 样式二
     - 样式三
     ```
     
   * 输出
   
     * 样式一
   
     + 样式二
   
     - 样式三

2. 有序列表

   * 输入

     ```markdown
     1. 表项一
     2. 表项二
     3. 表项三
     ```

   * 输出
     1. 表项一
     2. 表项二
     3. 表项三

3. 任务列表

   * 输入

     ```markdown
     - [ ] 不勾选
     - [x] 勾选
     ```

   * 输出

     - [ ] 不勾选

     - [x] 勾选



## 代码块

* 输入

  ```markdown
  ```javascript
  console.log("Hello World!");
  ​```
  ```

* 输出

  ```javascript
  console.log("Hello World!");
  ```



## 表格

* 输入

  ```markdown
  | 表头一 | 表头二 | 表头三 |
  | --- | --- | --- |
| 表项一 | 表项二 | 表项三 |
  ```

* 输出

  | 表头一 | 表头二 | 表头三 |
  | --- | --- | --- |
  | 表项一 | 表项二 | 表项三 |



## 脚注

* 输入

  ```markdown
  这是正文内容，这是一个需要注释的地方[^1]。
  [^1]: 这是对上面的注释
  ```

* 输出

  这是正文内容，这是一个需要注释的地方[^1]。

  [^1]: 这是对上面的注释



## 分割线

* 输入

  ```markdown
  ***
  ---
  ```

* 输出

  ***

  ---



## 链接

1. 网页链接

   * 输入

     ```markdown
     [百度一下](https://www.baidu.com/ "标题")
     ```

   * 输出

     [百度一下](https://www.baidu.com/ "标题")

2. 参考链接

   * 输入

     ```markdown
     这是正文内容，[百度一下][1]。
     [1]: https://www.baidu.com/
     ```

   * 输出

     这是正文内容，[百度一下][1]。

     [1]: https://www.baidu.com/

3. 图片链接

   * 输入

     ```markdown
     ![图片文字](./test.jpg)
     ```

   * 输出

     ![图片文字](./images/test.jpg)



## 字体样式

1. 加粗

   * 输入

     ```markdown
     **加粗的文字**
     ```

   * 输出

     **加粗的文字**

2. 倾斜

   * 输入

     ```markdown
     *倾斜的文字*
     ```

   * 输出

     *倾斜的文字*

3. 代码标记

   * 输入

     ```markdown
     `some code`
     ```

   * 输出

     `some code`

4. 删除线

   * 输入

     ```markdown
     ~~删除线~~
     ```

   * 输出

     ~~删除线~~

5. 表情符号

   * 输入

     ```markdown
     :smile:
     ```

   * 输出

     :smile:

6. 修改字体

   - 输入

     ```
     <font face=Times New Roman color = ff0000 size=4> My name is Shizheng Wen</font>
     ```

   - 输出

     <font face=Times New Roman color = ff0000 size=4> My name is Shizheng Wen</font>

   - 输入

     ```
     <font face=Times New Roman color = grey size=4> My name is Shizheng Wen</font>
     ```

   - 输出

     <font face=Times New Roman color = grey size=4> My name is Shizheng Wen</font>

   - 补充

     - 苹果电脑中的常用字体：
       Courier New、consolas、Times New Roman
     - 模版：`<font color=#FF0000 size=3 face=STHeiti>文本内容</font>`
       上面的模版代码中文本内容部分`可以加*,$等` （加粗，数学公式）相关的原markdown语法，不冲突
     - Size：规定文本的尺寸大小。可能的值：从 1 到 7 的数字。浏览器默认值是 `3`
     - Color：可以写16进制RGB（#FF0000或#ff0000）or 直接写名称（red）

7. 醒目标记（基于公示）

   - 输入

     ```
     $\bbox[green]{abc}$
     ```

   - 输出

     $\bbox[green]{abc}$





