# Python
  
# Python基本语法串讲

## 2.1-Linux指令、Hello World

-   python 运行Python解释器

-   python命令行中可以直接3+5*1

-   在python中，同样存在变量的概念  

-   变量，就是一个标签，由非数字开头的字母、数字、下划线组成，它的内容可以是数值、字符串、列表、元组和字典

-   字符串，就是用一对儿双引号、或单引号引起来的内容，只要被引号引起来，就是字符串了。b = "hello world"

-   在print 后的双引号内，还可以使用

-   转义字符：\t 表示 tab ；\n 表示换行 ；\"表示“

-   %s占位，用%后的变量替换

## 

2.2 Python中的数据类型

（就有点像英语中的单词）

1.  列表

1.  对于列表中元素的索引，python是0base的，而matlab是1base的。这点要注意！

2.  用c[ : ]对列表中元素做切片

3.  列表名[起：止：步长] 带步长的切片，步长有方向

4.  ......

2.  python数组

-   Python在标准库中有一个列表作为内置类型和一个标准库的array模块数组。这个数组不同于NumPy导出的多维数组

-   列表和数组与 numpy.ndarray之间的差异

-   列表 --list

-   数组 --array

-   多维数组 --numpy.ndarray

-   具体的内容可参考[CSDN](https://www.csdn.net/tags/OtDaMg1sMDI3MzktYmxvZwO0O0OO0O0O.html)

3.  元组

1.  誓言，一旦定义不能改变。 f= (1,2,3)

4.  字典

1.  字典里面放着n个键值对

2.  dic = {1:"123","name":"zhangsan","height":180}

3.  用字典名[键]索引字典中的值

## 

2.3 Python中的基本语句

1.  条件语句

2.  循环语句

1.  for 变量 in range (开始值，结束值):

执行某些任务

2.  for 变量 in 列表名:

执行某些任务

3.  while 条件:

执行某些任务

4.  循环终止用break

## 

2.4 函数、模块、包

1.  函数

1.  用def 函数名 (参数表)

    函数体

2.  模块（module）

1.  函数的集合：是一个python文件，以.py结尾，包含了Python函数等语句。先导入，再使用，用模块.函数名调用

3.  包

1.  包含有多个模块（也就是一个package里面含有很多个module，就是很多个python文件。每个python文件里面有含有很多个函数）

2.  from PIL import Image 从哪个包中导入哪个模块。

4.  变量作用域

1.  局部变量：在函数中定义的变量，只在函数中存在，函数执行结束不可再用。

2.  全局变量：在函数前定义的变量，一般在整个代码最前面定义，全局可用。

5.  类、对象和面向对象的编程 

1.  类（class）：用来描述具有相同的属性和方法的对象的集合。它定义了该集合中每个对象所共有的属性和方法。对象是类的实例。物以类聚人以群分，类是可实例化出对象的模具。

2.  对象：是类实例化出的实体，对象实实在在存在，完成具体工作。

3.  面向对象：程序员反复修改优化类，类实例化出对象，对象调用类里的函数执行具体的操作。

4.  类中每个对象具备的功能，在计算机中用函数的形式表示。

5.  类的继承：子类实例化出的对象，可以使用自身和父类的函数与变量

6.  类的定义：

class 类名 （父类名）:

   pass

7.  如果有父类，写在类名后面的括号里；如果没有父类，可以不写括号了。用关键词pass占个位置，之后再用具体函数把类补充完整

8.  **类里定义函数时，语法规定第一个参数必须是self 。【我之前看的代码中函数变量里的self值得原来是这个函数实在类里面进行定义的。】

9.  __init__ 函数，在新对象实例化时会自动运行，用于给新对象赋初值。

10.  模块.函数名 |  对象.函数名 | 对象.变量名  对象和模块挺像的，都是用xxx.xxx来调用其中的函数

11.  类内定义函数时，如调用自身或父类的函数与变量，须用self.引导，应写为self.函数名或self.变量名。

  

# 

Python常见错误

## 

如何找某一个array中的最值并返回其索引：

import numpy as np

  

X = result[:,1]

a=np.min(x)  # np.max

print(np.where(X==a))

[https://blog.csdn.net/songyunli1111/article/details/79322103](https://blog.csdn.net/songyunli1111/article/details/79322103)  这个网址里面介绍的比较全  

  

  

1.两数据恒等的问题，注意，如果是两数值型数据相等，要考虑他们的数据类型是否一样，不然的话是不能相等的。

eg.

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/zrHD4Gj0KLEqe_FyocQmldIP90_10w3KacoNuZf1X9M.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

就好比这句话，要判断size_input中提取出来的数据其类型是否和0.04是相等的。

##上面那句话说的有点问题，应该是只有在两数值型数据是否相等的时候才会遇到这种情况，判断谁比谁打，谁比谁小不会遇到这种问题。

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/HmDZYbvyq92enrhNDXukTOBz1IwjCKyrXl2-ZvO--ao.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

将上面那句话这样改就正确了

  

## 

对数组的相关操作，比如删除数组中的某一行

删除数组中的第一行

A = np.delete(inside_airfoil,0,0)

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/Ew-3W0WAYa9tb6Wv29Zvh8T0uI1oAudxcV9BNqAB4Gk.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

  

  

## 

改变一个数组的维度需要用np.reshape函数来进行实现

a_1 = np.reshape(test_photo_nobuffet, (1,100, 100, 3))

## 

spyder中清楚变量命令

-   清楚变量，在IPython中输入reset ，得到提示输入y确认即可

-   清空IPhython中输入历史记录，在控制台输入clear 即可，也可以使用快捷键Ctrl + L

  

  

# 

Python常用技巧

## 

如何将某个文件夹永久加入python路径中

Please add pyCaMOtk folder to your python path, so your system can find it, such as export PYTHONPATH=$PYTHONPATH:your_path/pycamotk

参考下面这个解释：

[https://www.cnpython.com/qa/38813](https://www.cnpython.com/qa/38813)

  

## 

数组array的转置。

直接用下面这个命令xcg.T 

  

## 

torch与numpy数据的转换及注意

-   python的基本数据类型就是：int，float，string以及更高级的list，tuple，dic。而更高级的三种其实有对象的属性。通常是a.append()这种方式调用该对象里面的函数。

-   当我们调用某些包时，这些包其实就是定义了一个新的类，我们可以将这些新的类实例化一些对象，然后用这个包里面的函数来对我们这个对象进行操作。科学计算常用的是array和tensor。而torch支持numpy中对数据的切片操作。我么你也可以灵活地将pytorch与numpy进行转化。

-   参考这个文档：[https://zhuanlan.zhihu.com/p/267824795](https://zhuanlan.zhihu.com/p/267824795)

-   [pytorch官方文档](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html)

-   [pytorch中文文档](https://pytorch-cn.readthedocs.io/zh/latest/package_references/torch/)

-   [NumPy中文文档](https://www.numpy.org.cn/user/quickstart.html#%E5%85%88%E5%86%B3%E6%9D%A1%E4%BB%B6)

-   [NumPy官方文档](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.html)

-   需要注意的是，如果想用GPU进行运算，我们需要定义能在GPU上运算地CUDA tensors。需要注意的是Tensors can be moved onto any device using the .to method

-   张量实在深度学习框架中的一个数据结构，把数据喂进模型中需要把数据转化为tensor结构，等我们再取出来做框架以外的操作，比如保存成文件，用plot画图，都需要重新转换成array或list结构。

-   list转array array = np.array(list) 

-   list转torch.Tensor tensor = torch.Tensor(list) 

-   我们在一般定义变量是都是用的这两种方法，都是直接调用各个包的函数

-   array转torch.Tensor tensor = torch.from_numpy(array)

-   torch.Tensor转arrayarray = tensor.numpy() gpu情况需要进行如下操作array = tensor.cpu().numpy() 

-   以上两种也是常用结构，其中，array转tensor调用的是torch包的函数，而tensor转array则调用tensor这个类里面的函数。

-   torch.Tensor转list #先转numpy，后转list list = tensor.numpy().tolist()

-   array转list list = array.tolist()

-   我们很容易用numpy()和from_numpy()将Tensor和NumPy中的数组相互转换。但是需要注意的一点是： 这两个函数所产生的的Tensor和NumPy中的数组共享相同的内存（所以他们之间的转换很快），改变其中一个时另一个也会改变！！！

-   还有一个常用的将NumPy中的array转换成Tensor的方法就是torch.tensor(), 需要注意的是，此方法总是会进行数据拷贝（就会消耗更多的时间和空间），所以返回的Tensor和原来的数据不再共享内存。

-   我们还可以使用类似NumPy的索引操作来访问Tensor的一部分，需要注意的是：索引出来的结果与原数据共享内存，也即修改一个，另一个会跟着修改。

-   前面说了，索引操作是不会开辟新内存的，而像y = x + y这样的运算是会新开内存的，然后将y指向新内存。为了演示这一点，我们可以使用Python自带的id函数：如果两个实例的ID一致，那么它们所对应的内存地址相同；反之则不同。

  

# 

Numpy学习

-   [NumPy中文文档](https://www.numpy.org.cn/user/quickstart.html#%E5%85%88%E5%86%B3%E6%9D%A1%E4%BB%B6)

-   [NumPy官方文档](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.html)

## 

基础知识

NumPy的数组类被调用ndarray。它也被别名所知 array。请注意，numpy.array这与标准Python库类不同array.array，后者只处理一维数组并提供较少的功能。ndarray对象更重要的属性是：

-   ndarray.ndim - 数组的轴（维度）的个数。在Python世界中，维度的数量被称为rank。

-   ndarray.shape - 数组的维度。这是一个整数的元组，表示每个维度中数组的大小。对于有 n 行和 m 列的矩阵，shape 将是 (n,m)。因此，shape 元组的长度就是rank或维度的个数 ndim。

-   ndarray.size - 数组元素的总数。这等于 shape 的元素的乘积。

-   ndarray.dtype - 一个描述数组中元素类型的对象。可以使用标准的Python类型创建或指定dtype。另外NumPy提供它自己的类型。例如numpy.int32、numpy.int16和numpy.float64。

-   ndarray.itemsize - 数组中每个元素的字节大小。例如，元素为 float64 类型的数组的 itemsize 为8（=64/8），而 complex32 类型的数组的 itemsize 为4（=32/8）。它等于 ndarray.dtype.itemsize 。

-   ndarray.data - 该缓冲区包含数组的实际元素。通常，我们不需要使用此属性，因为我们将使用索引访问数组中的元素。

【在python标准库类也存在array这种对象，通常是用array.array() 来进行创建，但需要注意的是，这种一般只能处理少量的一维数组，并且只能提供较少的功能，也就是较少的函数对象。】

## 

常见问题

### 

Python列表_和_数组与_numpy_._ndarray_的区别_和_使用方法

主要是再用torch.from_numpy()时出现错误，这种转换只能适用于numpy实例化的多维数组，而不能用于内置数组数据库中的array。具体可参考[CSDN](https://www.csdn.net/tags/OtDaMg1sMDI3MzktYmxvZwO0O0OO0O0O.html)

出现此错误时将[torch](https://so.csdn.net/so/search?q=torch&spm=1001.2101.3001.7020).from_numpy()改为torch.Tensor()即可

# 

PyTorch+Python学习

-   [pytorch官方文档](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html)

-   [pytorch中文文档](https://pytorch-cn.readthedocs.io/zh/latest/package_references/torch/)

  

## 

小的Tips

1.  在进行python代码编程的时候，通常可以先给定义变量，这一步包括变量的类型，变量的大小和形状。之后在程序里面给之前定义好的变量进行赋值。在对变量进行赋值的时候，我们习惯使用U[:]=a[:]; U[:]=0.0 这种形式，为了防止内存的误用。这是非常有用的技巧。

## 

常见错误

### 

01 个人编程遇到小问题

-   torch.mm(A,B) 两个矩阵相乘，但是，这个函数要求相乘的两个矩阵具有同样的数据精度，都为float或者都为double。而A*B 这种不调用函数的元素乘则不会有这个问题。可在Tensor后面加.long() .int() .float() .double() 等，也可用.to() 函数进行转换。

-   在loss.backward()之后，如果我们还要调用调用loss这个变量，不要直接写loss，不然会导致显存爆炸，直接用loss.item()来调用loss

-   可以用[MSE](https://pytorch.org/docs/stable/generated/torch.nn.MSELoss.html)来直接算二范数求loss，比torch.norm 要方便的多

-   当我将一个list of tensors用torch.tensor() 转换成tensor时会报错，系统告诉我only one element tensors can be converted to Python scalars

-   这里给了一个解释，但似乎没什么用，不过很有学习意义：[csdn](https://blog.csdn.net/qq_38703529/article/details/120216078)

-   **我们可以用如下方式：首先，定义一个和这个list of tensors一样大的tensor。然后用torch.cat(Re_,axis=1) 来实现，这个方法就很巧妙了。

-   一般这种先搞一个list，然后再将tensor append进去，比如ReList.append() 通常是用来做叠加的。后面一般会写for i in range(len(ReList)):

loss = loss + ReList[i] 

-   Tensorflow Tensorboard报错：“No dashboards are active for the current data set.“ 解决方案 原因分析。主要是terminal当前的路径可能不在logs文件夹所处的位置，从而导致网络不存在这样一个log文件

-   assert函数：

def zeros(s):

    a = int(s)

   assert a > 0, "a超出范围" # 这句话的意思：如果a确实大于0，程序正常往下运行

   return a

  

zeros("-2") #但是如果a是小于0的，程序会抛出AssertionError错误，报错为参数内容”a超出范围“

-   torch.nn.Parameter()函数，在网络中定义，将网络中一个tensor类型的量转换成网络可以训练的parameter，也就是可以反向求解梯度的。

-   try和except函数

-   首先，我们先介绍这个怎么用,try-except是用来引发异常，所以，程序执行的时候，首先会执行try部分，如果try报错，就会执行except部分，如果try部分没有报错，程序就会跳过except部分执行。[百度百科](https://jingyan.baidu.com/article/851fbc37a16f0c3e1f15abd6.html)

-   网络权重的初始化，用torch.nn.init.orthogonal_(tensor, gain=1) [详细参考官网](https://pytorch.org/docs/stable/nn.init.html)

-   索引小技巧

-   pred, gt = output[0:-1:40, :, ::2, ::2], truth[::40,:, ::2, ::2].cuda()  
    这里的意思是每个四十行取一个结果。

-   如何查看pytorch对应的cuda版本

import torch

print(torch.version.cuda)

-   退出python的三种方法

-   exit()

-   quit()

-   ^Z

-     
    

  

### 

02 PyCharm本地远程连接服务器

1.  首先，下载教育版的Xshell(命令行管理)和Xftp7(传输文件)。再得知远程服务器的地址以及相应的账号和密码，即可远程登陆服务器。按道理来说我们装了GPU，应该是有图形界面

1.  可参考这个[bilibili](https://www.bilibili.com/video/BV1DZ4y1W7ib/?spm_id_from=333.788.recommend_more_video.2)

ssh -l shizhengwen -p 22 shizhengwen@129.10.99.214

shizhengwen123

2.  在本地服务器上先下载Linux版本的anaconda，然后用Xftp7传输到远程服务器上，再远程服务器上依次解压，得到我们的conda环境

1.  可参考这个 [地址](https://mp.weixin.qq.com/s?__biz=Mzg2MzE2MzUxMg==&mid=2247484519&idx=1&sn=fb47368d84448401a610459f0169782b&scene=19#wechat_redirect) 【这个公众号里面有非常详细地环境配置步骤，可以好好看一看，或者看他的[bilibili](https://www.bilibili.com/video/BV1yb411T7zs?spm_id_from=333.999.0.0)】

2.  这一步要主要Linux安装anaconda3是否初始化的区别，记得选yes，选no也没关系，参考这个[CSDN](https://blog.csdn.net/qq_41126685/article/details/105525408)

3.  接着在上面安装我们需要的python编译环境，老版本python见: [官网](https://pytorch.org/get-started/previous-versions/)

# 之前我python版本装的太高了也不行，我重装了一个Python3.8的环境，搭配10.1的CUDA就好了，直接用官网的

pip install torch==1.8.1+cu101 torchvision==0.9.1+cu101 torchaudio==0.8.1 -f https://download.pytorch.org/whl/torch_stable.html

对于pyg的安装，如果用pip进行安装，一定手动安装，不要用它提供的自动安装模式，这是血与泪的教训，可参考这个[bilibili](https://www.bilibili.com/video/BV1eS4y1o7PE?spm_id_from=333.999.header_right.fav_list.click)

老版[PyTorch官网](https://pytorch.org/get-started/previous-versions/) [PyTorch官网](https://pytorch.org/get-started/locally/)

[pyg项目](https://github.com/pyg-team/pytorch_geometric)

3.  用professional版本的pycharm和远程服务器进行连接 [weibo](https://weibo.com/ttarticle/p/show?id=2309404538923987632130&sudaref=www.baidu.com)

1.  可参考这个 [知乎](https://zhuanlan.zhihu.com/p/259683970)

非常有用的视频教程

1.  Pycharm用ssh连接远程服务器 [bilibili](https://www.bilibili.com/video/BV1qQ4y1N7K1?spm_id_from=333.337.search-card.all.click)

2.  JupyterLab用ssh连接服务器 [bilibili](https://www.bilibili.com/video/BV1k34y1t7gu/?spm_id_from=333.788.recommend_more_video.1)

  

注意：

数据的拷贝问题。说下远程服务器连接运行的原理，本地起到的作用是什么呢？其实本地pycharm只是一个记事本的功能，根本不具备代码运行的能力。但是有了这个“记事本”，我们可以随心所欲的修改代码，然后马上执行，调试非常方便。假如没有这个pycharm，我们需要在f开头那个数据上传软件重新覆盖上传。非常麻烦。  
那最终代码是怎么运行的呢？先由pycharm发送运行命令，然后远程服务器开始执行代码，如果代码运行时出现路径问题，是因为代码里面路径写了绝对路径，服务器可没d盘啥的，需要修改为相对路径。最后运行完，生成的模型，也是留在服务器，需要手动下载到本地。一句话，pycharm本地可以同步代码到服务器，但是当数据变动以后，服务器不能自动同步到本地电脑。

-   也就是说，这里只是代码上可以进行同步，但是像数据集，文件夹，模型之类的还是需要手动上传和下载，这个用Xftp来进行实现就可以，似乎也可以直接在pycharm里面选择下面这个查看修改。

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/xlPO1OfqxKAZ3u7wns9sySTkUr28ej2ngBNZBxFgLQw.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/2bZM44h1iplMKrLOj60KecwbuxIcXf3WiRI8P-fdA9s.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

  

  

### 

03 Pytorch中如何指定GPU

1.  为什么要指定GPU

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/NhKQ-aFQvLw-s7AOLIQrdPDwT4P87sAiIsvy6ViC9h0.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

Ref: [bilibili](https://www.bilibili.com/video/BV15E411u7tV/?spm_id_from=333.788.recommend_more_video.1)

2.  如何指定GPU

import os

os.environ["CUDA_VISIBLE_DEVICES"] = "1"

方法：  
用这两行代码  
需要放在整个.py文件的最开头，在调用torch之前就要用，不然无效。

### 

04 Nvidia A100显卡驱动安装

关于CUDA版本的一些问题： [知乎](https://zhuanlan.zhihu.com/p/466907729)

### 

05 Pytorch和CUDA版本对应关系

参考这篇链接：[https://www.cnblogs.com/zhoujiayingvana/p/15827369.html](https://www.cnblogs.com/zhoujiayingvana/p/15827369.html)

### 

06 Pycharm-专业版免费安装

参考这篇说明：[https://zhuanlan.zhihu.com/p/338280181](https://zhuanlan.zhihu.com/p/338280181)

### 

07 torch.Tensor与torch.tensor之间的区别。

[https://blog.csdn.net/weixin_42018112/article/details/91383574](https://blog.csdn.net/weixin_42018112/article/details/91383574)

torch.Tensor()是Python类，更明确的说，是默认张量类型torch.FloatTensor()的别名，torch.Tensor([1,2]) 会调用Tensor类的构造函数__init__，生成单精度浮点类型的张量。

torch.tensor()仅仅是Python的函数，函数原型是：

torch.tensor(data, dtype=None, device=None, requires_grad=False)

其中data可以是：list, tuple, array, scalar等类型。  
torch.tensor()可以从data中的数据部分做拷贝（而不是直接引用），根据原始数据类型生成相应的torch.LongTensor，torch.FloatTensor，torch.DoubleTensor。

### 

08 Pytorch常见的Tensor类型详解

[https://www.zongscan.com/demo333/88121.html](https://www.zongscan.com/demo333/88121.html)

  

### 

09 代码中网络参数类型不统一

[https://blog.csdn.net/weixin_43977647/article/details/112573373](https://blog.csdn.net/weixin_43977647/article/details/112573373)

[https://blog.csdn.net/ttdxtt/article/details/112347283](https://blog.csdn.net/ttdxtt/article/details/112347283)

但是我没有测试过是否可行！！

  

### 

10 Tensor.detach()

tensor.detach():

 从计算图中脱离出来，返回一个新的tensor，新的tensor和原tensor共享数据内存，（这也就意味着修改一个tensor的值，另外一个也会改变），但是不涉及梯度计算。在从tensor转换成为numpy的时候，如果转换前面的tensor在计算图里面（requires_grad = True），那么这个时候只能先进行detach操作才能转换成为numpy.

见csdn：[https://blog.csdn.net/m0_47746932/article/details/119598396](https://blog.csdn.net/m0_47746932/article/details/119598396)

  

但是因为新的tensor和原tensor同样是共享内存的，所以我并不知道新的tensor变化为numpy后是否会对原tensor的网络训练产生影响

  

### 

11 model.train()和model.eval()

-   在使用pytorch构建神经网络的时候，训练过程中会在程序上方添加一句model.train()，作用是启用batch normalization和drop out。

-   测试过程中会使用model.eval()，这时神经网络会沿用batch normalization的值，并不使用drop out。

  

### 

12 cuda上不能进行torch中的转置和求行列式操作

-   如果我们将一个tensor.cuda()到GPU上，那么，我们不能用torch自带的求转置和求逆的函数对其进行操作。要不然就是自己写函数，要不然就是先以numpy的形式算完逆和转职后再将其转移到GPU上。

  

### 

13 PyCharm中的terminal运行前面的PS如何修改成自己环境

主要还是进入Terminal修改shell path。这对我直接在PyCharm里面安装宝以及调整tensorboard非常有用。

  

### 

14 GPU相比于CPU没有明显的加速

nvidia-smi

-   可能是因为batch size设置的很小或者网络比较小：

-   [https://www.zhihu.com/question/345418003](https://www.zhihu.com/question/345418003)

-   [https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html#training-on-gpu](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html#training-on-gpu)

-   先看一下batch_size的概念：[https://www.jiqizhixin.com/articles/2018-07-12-4](https://www.jiqizhixin.com/articles/2018-07-12-4)

-   [深入探讨！Batch大小对训练的影响](https://blog.csdn.net/red_stone1/article/details/119657578)

-   [windows10下pytorch的GPU利用率底，占用率低](https://blog.csdn.net/stay_zezo/article/details/107809409)

-   [有关Pytorch训练时Volatile Gpu-Util(GPU利用率)很低，而Memory-ueage(内存占比)很高的情况解释与说明](https://blog.csdn.net/qq_44554428/article/details/122751996)

-   有的网友说batchsize = 1也能一定情况下加速运算，主要原因是可以更方便地进行矩阵运算[https://www.zhihu.com/question/477794792/answer/2049476711](https://www.zhihu.com/question/477794792/answer/2049476711)

  

### 

15 图网络 torch_geometric

1.  [百度](https://www.baidu.com/s?ie=utf-8&f=8&rsv_bp=1&rsv_idx=2&tn=baiduhome_pg&wd=torch_geometric&rsv_spt=1&oq=normalization%253Dsym&rsv_pq=82fd1ddd000936ec&rsv_t=704dD80plc0P7knazFnC%2FFKOZ9Kk6Ds7cZDcbJ8%2F1%2BSckqOaDdSsEd2aSktDxv6c%2Babh&rqlang=cn&rsv_dl=tb&rsv_enter=1&rsv_sug3=2&bs=normalization%3Dsym)

2.  [知乎](https://zhuanlan.zhihu.com/p/94491664)

3.  [知乎](https://zhuanlan.zhihu.com/p/477327735)

4.  [CSDN](https://blog.csdn.net/qq_40206371/article/details/120619459)

  

### 

16 torch中tensor变量的赋值问题

a=torch.zeros([1,2]) # 也可以写成torch.zeros((1,2))一个是通过元组创建，一个是通过list创建

a[:]=1

print(a) #最后输出的是tensor([1.,1.])

  

# 如果是下面这种表示

a=torch.zeros([1,2]) # 也可以写成torch.zeros((1,2))一个是通过元组创建，一个是通过list创建

a=1

print(a) #最后输出的是int型1。这种就是把1重新又赋值给了a

  

### 

17 关于python里面数据类型及其精度问题

对于float32（单精度）来说，表示尾数的为23位，除去全部为0的情况以外，最小为2-23，约等于1.19*10-7，所以float小数部分只能精确到后面6位，加上小数点前的一位，即有效数字为7位。

同理float64（单精度）的尾数部分为52位，最小为2-52，约为2.22*10-16，所以精确到小数点后15位，加上小数点前的一位，有效位数为16位。

[百度百科](https://zhidao.baidu.com/question/881665421259763692.html)

  

-   在我用loss.item() 输出误差时，最后的误差时float类型，而不是np.float64或者torch.float64。即不是外包程序自带的数据对象。

  

### 

18 关于变量赋值的问题

在python里面，如果想要将一个变量的值赋给另一个变量，用a=b这种方式通常会出错，因为这是一种内存不会重新分配，可以采用先给a和b分别内存，然后再用a[:]=b[:] 进行变量的赋值

  

### 

19 Torch里面关于squeeze和unsqueeze函数的使用

Ref: [csdn](https://blog.csdn.net/xiexu911/article/details/80820028)

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/KkbeiOXP2d6D3HuddfJpWNMJKfJRHg2LvYhICD-fyqE.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

用了squeeze函数后我们可以使用torch.cat函数去append a tensor to a list tensor

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/yoMX6tcik8mMK79R39hwkQJgE--q8alkxjpFQvDXnVs.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

Ref: [https://discuss.pytorch.org/t/how-to-append-an-int-tensor-to-a-list-tensor/106939/5](https://discuss.pytorch.org/t/how-to-append-an-int-tensor-to-a-list-tensor/106939/5)

见如下两种方式来append变量

conn=np.append(conn,conn[0])

conn=torch.cat([conn,conn[0].unsqueeze(0)])

### 

20 Tensor里面的索引必须得是long类型

也就是tensor里面的索引被削得是64 int型。

  

### 

21 Tensor里面的操作必须都针对tensor对象，而不是float

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/aivjfbabJwNg5vcIKrU86kaJNlXnXNGxYP6PkEFBmCs.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

  

### 

22 Torch和Numpy对比

-   以我目前的经验来看，tensor如果不挂在cuda上，速度不如numpy。

torch比numpy慢。  
numpy是python中处理数据的模块，可以处理各种的矩阵(matrix)。  
Torch自称为神经网络中的numpy。它会将torch产生的tensor放在GPU中加速运算，就像numpy会把array放在CPU中加速运算。

Torch与Numpy对比：

[CSDN1](https://blog.csdn.net/qq_43391414/article/details/120488436?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_title~default-0-120488436-blog-114681718.pc_relevant_antiscanv3&spm=1001.2101.3001.4242.1&utm_relevant_index=3)

[CSDN2](https://viatorsun.blog.csdn.net/article/details/106862863?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-2-106862863-blog-120488436.pc_relevant_aa&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-2-106862863-blog-120488436.pc_relevant_aa&utm_relevant_index=5)

  

### 

23 在PyTorch框架下使用PyG和networkx对Graph进行可视化

[https://zhuanlan.zhihu.com/p/92482339](https://zhuanlan.zhihu.com/p/92482339)

  

### 

24 python去除二维数组中的重复行

[https://www.qb5200.com/article/342393.html](https://www.qb5200.com/article/342393.html)

[https://wenku.baidu.com/view/585245f2350cba1aa8114431b90d6c85ec3a881a.html](https://wenku.baidu.com/view/585245f2350cba1aa8114431b90d6c85ec3a881a.html)

  

### 

25 python中过于内存公用的问题

问题：最开始我在epoch循环外面定义

best_loss=torch.tensor([20])

batch_loss=torch.zeros([1])

之后在epoch循环里面采用

batch_loss[:]=0

  

batch_loss=loss.item()

  

   if batch_loss < best_loss:

        save_checkpoint(model, optimizer, scheduler, save_path)

       print('successfully save the model')

        best_loss=batch_loss[:]

总是会出现best loss和batch loss公用一个内存的情况。

  

### 

26 *Pytorch关于拷贝和就地操作

CSDN: [https://blog.csdn.net/weixin_43199584/article/details/106770647](https://blog.csdn.net/weixin_43199584/article/details/106770647)

需要注意的是，虽然就地操作有助于使用更少的GPU内存。但torch变量带requires_grad 的不能进行in-place operation（就地操作）[CSDN](https://blog.csdn.net/jacke121/article/details/82733407?spm=1001.2101.3001.6650.1&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7EPayColumn-1-82733407-blog-123449024.pc_relevant_default&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7EPayColumn-1-82733407-blog-123449024.pc_relevant_default&utm_relevant_index=1) [教程](https://www.nhooo.com/note/qah4u1.html)

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/YcocgUnoJ8O4FFFBK5mhOpJmeK_rPOXYLGkABK02Uf4.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

import torch # import main library

import torch.nn as nn # import modules like nn.ReLU()

import torch.nn.functional as F # import torch functions like F.relu() and F.relu_()

  

def get_memory_allocated(device, inplace = False):

   '''

    Function measures allocated memory before and after the ReLU function call.

    INPUT:

      - device: gpu device to run the operation

      - inplace: True - to run ReLU in-place, False - for normal ReLU call

    '''

   # Create a large tensor

    t = torch.randn(10000, 10000, device=device)

   # Measure allocated memory

    torch.cuda.synchronize()

    start_max_memory = torch.cuda.max_memory_allocated() / 1024**2

    start_memory = torch.cuda.memory_allocated() / 1024**2

   # Call in-place or normal ReLU

   if inplace:

        F.relu_(t)

   else:

        output = F.relu(t)

   # Measure allocated memory after the call

    torch.cuda.synchronize()

    end_max_memory = torch.cuda.max_memory_allocated() / 1024**2

    end_memory = torch.cuda.memory_allocated() / 1024**2

   # Return amount of memory allocated for ReLU call

   return end_memory - start_memory, end_max_memory - start_max_memory

   # setup the device

device = torch.device('cuda:0' if torch.cuda.is_available() else "cpu")

#开始测试

# Call the function to measure the allocated memory for the out-of-place ReLU

memory_allocated, max_memory_allocated = get_memory_allocated(device, inplace = False)

print('Allocated memory: {}'.format(memory_allocated))

print('Allocated max memory: {}'.format(max_memory_allocated))

'''

Allocated memory: 382.0

Allocated max memory: 382.0

'''

#Then call the in-place ReLU as follows:

memory_allocated_inplace, max_memory_allocated_inplace = get_memory_allocated(device, inplace = True)

print('Allocated memory: {}'.format(memory_allocated_inplace))

print('Allocated max memory: {}'.format(max_memory_allocated_inplace))

'''

Allocated memory: 0.0

Allocated max memory: 0.0

'''

  

  

---

下面开始研究我自己的代码：

  

对于我自己的问题，再第一次epoch后，本来不具有梯度计算能力的R就具有了梯度计算能力。这时候如果我在对R做就地操作，自然就会报错。因此我才在每一次epoch后都重新给R分配内存。但是这也牵扯出来另一个问题，之前的内存是否会被释放？

![](https://vipkshttps15.wiz.cn/editor/61df5710-321a-4abe-b23d-e224f0a20e93/2431066a-d8fd-481e-9b47-60d8a53848cb/resources/sAK76kWn-BeU2vJoBkiP74uOsQbQG1g9SKheNSwfxCY.png?token=W.-5v28sJTReUhjgPNuKF0mQHdE4NBKFJ8tRYHDmZvpSOnYgg)

在这个地方，我们可以看到，phi，gradphi和R都进行了就地操作，且这三个变量在第一次epoch之后都具有梯度。有梯度的变量在进行第二次epoch的就地操作后，反向传播则会出现问题。

此外，不太清楚这个过程中内存的使用情况大概是怎么样的。是否会释放之前的内存。可以看到这里写个函数还是很方便的，因为只存在局部变量。