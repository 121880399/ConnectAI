## 前文提要

在上一小节中，我们讲述了什么是导数，以及导数的基本性质。这一小节将更深入的理解导数。

## 1.偏导数

在之前的章节中我们讲了，对于函数y=f(x),x为自变量，y为因变量。这种函数只有一个自变量。

如果是函数z=f(x,y)那么这时候有就两个自变量（x,y）。我们通常将有两个以上的自变量函数称为**多变量函数**。

那么在多变量函数中，我们如何对其进行求导呢？

由于多变量函数存在多个变量，在求导时，我们必须指明要对哪一个变量进行求导。那么关于某个特定变量的导数就称为**偏导数**。

例如：函数 z = f(x,y)，分别求关于x的偏导数和关于y的偏导数。

$$\frac{\partial z}{\partial x} = \frac{\partial f(x,y)}{\partial x} = \lim_{\Delta x \to 0} \frac{f(x+ \Delta x,y) - f(x,y)}{\Delta x}$$

$$\frac{\partial z}{\partial y} = \frac{\partial f(x,y)}{\partial y} = \lim_{\Delta y \to 0} \frac{f(x,y+ \Delta y) - f(x,y)}{\Delta y}$$

从公式中我们可以看出来，在求关于x的偏导数时，我们把y看做了普通的常量。在求关于y的偏导数时，我们把x看做了普通的常量。

所以我们可以知道

> 在求关于某个变量的偏导数时，把其他的变量当作常数

看一个例子：当 $z = w_1x_1 + w_2x_2 + b_1$ 时，求关于x1,x2,b1的偏导数。

这是一个多变量函数，其中$w_1$,$x_1$,$w_2$,$x_2$,$b_1$都是自变量。

当求$x_1$的偏导数时，将其他所有变量都当作常量。

$$\frac{\partial z}{ \partial x_1} = w_1$$

当求$x_2$的偏导数时，将其他所有变量都当作常量。

$$\frac{\partial z}{ \partial x_2} = w_2$$

当求$b_1$的偏导数时，将其他所有变量都当作常量。

$$\frac{\partial z}{ \partial b_1} = 1$$

## 2.多变量函数的最小值

当函数f(x)在x=a 处取得最小值时，$f^\prime(a) = 0$。那么对于多变量函数来说，取得最小值的必要条件是什么呢？

答案就是偏导数都为0。

来看一个例子：求$z = x^2 + y^2$取得最小值时，x、y的值。

我们知道函数取得最小值时，关于x的偏导和关于y的偏导都为0。

$$\frac{\partial z}{\partial x} = 2x = 0$$

$$\frac{\partial z}{\partial y} = 2y = 0$$

那么就可以求出，x=0,y=0。


## 3.链式法则

现在我们知道了单变量函数求导，多变量函数求导。那么接下来我们一起看看复合函数求导。

#### 3.1 复合函数

所谓复合函数（Composite Function）是指一个函数的输入是另一个函数的输出。换句话说，复合函数通过“嵌套”两个或多个函数，将一个函数的输出作为另一个函数的输入来进行计算。

设有两个函数f(x)和g(x)，则它们都复合函数可以表示为f(g(x))，也可以写作$(f \quad o \quad g)(x)$。这表示现对x应用g(x)，然后再将g(x)的结果带入到f(x)中。

例如：设 

- $f(x) = 2x + 3$
- $g(x) = x^2$

那么复合函数f(g(x))就是：

  $$f(g(x)) = f(x^2) = 2(x^2) + 3 = 2x^2 + 3$$

如果x = 2，那么f(g(x))的值为：
 $$f(g(x)) = f(4) = 2 \times 4 + 3 = 11$$

#### 3.2 复合函数求导 

好，现在我们已经清楚了什么是复合函数，那么我们接下来看看如何对复合函数求导。

要对复合函数求导，我们需要使用链式法则。它的基本思想是先对外层函数求导，再乘以内层函数的导数。

如果y=f(g(x)),则复合函数的导数为：

$$\frac{dy}{dx} = f^\prime (g(x)) \cdot g^\prime(x)$$

即先对外层函数f求导，然后将内层函数g(x)代入，再乘以内层函数g(x)的导数。

看一个简单的例子：

设$f(x) = 2x+3 ,g(x)=x^2$,求$y=f(g(x)) = 2x^2 +3$的导数。

1.首先我们设$u=g(x)=x^2$。

2.然后我们求外层函数的导数。$f^\prime(u) = 2$。

3.接着求内层函数$g(x) = x^2$的导数，得到$g^\prime(x) = 2x$

4.应用链式法则:

  $$\frac{dy}{dx} = f^\prime(g(x)) \cdot g^\prime(x) = 2 \cdot 2x = 4x$$

所以复合函数$f(g(x) = 2x^2 +3$的导数为 4x。

#### 3.3 多变量复合函数求偏导

那么对多变量的复合函数求偏导要怎么利用链式法则呢？

如果复合函数$z = f(g_1(x,y),g_2(x,y))$,即z是x和y的函数，但通过$g_1(x,y)$和$g_2(x,y)$间接依赖x和y,则z对x和y的偏导数分别为：

$$\frac{\partial z}{\partial x} = \frac{\partial f}{\partial g_1} \cdot \frac{\partial g_1}{\partial x} + \frac{\partial f}{\partial g_2} \cdot \frac{\partial g_2}{\partial x}$$

$$\frac{\partial z}{\partial y} = \frac{\partial f}{\partial g_1} \cdot \frac{\partial g_1}{\partial y} + \frac{\partial f}{\partial g_2} \cdot \frac{\partial g_2}{\partial y}$$

举个例子：
设$z=f(u,v)=u^2+v$,其中$u = x^2 + y ,v = x + y^2$。我们想计算$\frac{\partial z}{\partial x}$和$\frac{\partial z}{\partial y}$。

**步骤1**：求f(u,v)对u和v的偏导数。

$$\frac{\partial f}{\partial u} = 2u$$

$$\frac{\partial f}{\partial v} = 1$$

**步骤2**:求$u = x^2 + y ,v = x + y^2$关于x和y的偏导数。

$$\frac{\partial u}{\partial x} = 2x$$

$$\frac{\partial u}{\partial y} = 1$$

$$\frac{\partial v}{\partial x} = 1$$

$$\frac{\partial v}{\partial y} = 2y$$

**步骤3**:应用链式法则求$\frac{\partial z}{\partial x}$和$\frac{\partial z}{\partial y}$。

对x的偏导：

$$\frac{\partial z}{\partial x} = \frac{\partial f}{\partial u} \cdot \frac{\partial u}{\partial x} + \frac{\partial f}{\partial v} \cdot \frac{\partial v}{\partial x} = 2u \cdot 2x + 1 \cdot 1 = 2(x^2 + y) \cdot 2x + 1 = 4x(x^2 +y) +1$$

对y的偏导：

$$\frac{\partial z}{\partial y} = \frac{\partial f}{\partial u} \cdot \frac{\partial u}{\partial y} + \frac{\partial f}{\partial v} \cdot \frac{\partial v}{\partial y} = 2u \cdot 1 + 1 \cdot 2y = 2(x^2 + y) \cdot 1 + 2y = 2x^2+4y$$

#### Softmax和交叉熵函数组合而成的复合函数

我们现在来看一个稍微复杂一点的例子，我们前面介绍了Softmax函数，知道该函数是应用在输出层的激活函数，主要的作用是将输出层的输出值转换为概率值。而交叉熵函数是损失函数，用于衡量预测概率分布与真实概率分布之间的差异。

我们来回顾一下这两个函数的公式：

**1.Softmax函数：**

$$\sigma (z_i) = \frac{e^{z_i}}{\sum_{j=1}^n e^{z_j}}$$

其中$z_i$表示第i个节点的加权输入值，$\sigma (z_i)$是第i个节点的预测概率。

**2.交叉熵函数:**

$$L = - \sum_{i=1}^n y_i log\widehat{y_i}$$

其中$y_i$是第i个目标变量，这里假设使用one-hot编码，也就是只有正确的节点y=1，其余节点y=0。$\widehat{y_i}$是Softmax的输出值。

那么将这两个函数组合在一起就是一个复合函数:

$$L = - \sum_{i=1}^n y_i log(\sigma (z_i))$$

好，现在要对这个复合函数求关于$z_i$的偏导该如何求？

我们先求$\frac{\partial L}{\partial \sigma (z_i)}$

这里涉及我们上一小节讲过的，对求和函数求导。我们先将求和函数展开：

$$L = -[(y_1log(\sigma (z_i))) + (y_2log(\sigma (z_i))) + ... + (y_nlog(\sigma (z_i)))]$$

由于我们使用的是one-hot编码，所以这里的y只有1个节点为1，其余节点都为0。那么公式就可以化简为：

$$L = -(y_ilog(\sigma (z_i)))$$

由于对数函数的求导公式为$log(\sigma (z_i)) = \frac{1}{\sigma (z_i)}$,所以$\frac{\partial L}{\partial \sigma (z_i)}$为：

$$\frac{\partial L}{\partial \sigma (z_i)} = - \frac{y_i}{\sigma (z_i)}$$

接下来求$\frac{\partial \sigma (z_i)}{\partial z_i}$:

这里需要考虑两种情况：

1.当i = j时，这种情况指的是输入是$z_i$,也对$z_i$求导：
$$\frac{\partial \sigma(z_i)}{\partial z_i}$$

根据商的求导法则：

$$\frac{d}{dx}(\frac{f(x)}{g(x)}) = \frac{f^\prime(x)g(x)-f(x)g^\prime(x)}{g(x)^2}$$

逐步求解：
- 分子$f(z_i) = e^{z_i}$,其导数$f^\prime(z_i) = e^{z_i}$。
- 分母$g(z_i) = \sum_{j=1}^n e^{z_j}$,其导数为$e^{z_i}$,因为除了$e^{z_i}其他的全是常数，求导为0。$

代入后得：

$$\frac{\partial \sigma(z_i)}{\partial{z_i}} = \frac{e^{z_i} \cdot \sum_{j=1}^n e^{z_j} - e^{z_i} \cdot e^{z_i}}{(\sum_{j=1}^n e^{z_j})^2}$$

化简公式：

$$\frac{\partial \sigma(z_i)}{\partial{z_i}} = \frac{e^{z_i}(\sum_{j=1}^n e^{z_j} - e^{z_i})}{(\sum_{j=1}^n e^{z_j})^2} = \frac{e^{z_i}}{\sum_{j=1}^n e^{z_j}} \cdot (1 - \frac{e^{z_i}}{\sum_{j=1}^n e^{z_j}}) = \sigma (z_i)(1-\sigma (z_i))$$

2.当 $i \neq j$时，这种情况指的是输入是$z_j$,但是对$z_i$求导，其目的是考虑$z_i$的变化是如何影响到其他类别($\sigma(z_j)$)的输出概率。

$$\frac{\partial \sigma(z_j)}{\partial z_i} (当i \neq j)$$

这种情况下，分子$f(z_j) = e^{z_j}$，其导数为0，因为$e^{z_j}$与$z_i$是无关的。

分母$g(z_i) = \sum_{k=1}^n e^{z_k}$,其导数为$e^{z_i}$,因为其中包括$z_i$项,其他项的导数为0。

代入公式：
$$\frac{\partial \sigma(z_j)}{\partial{z_i}} = \frac{0 \cdot \sum_{k=1}^n e^{z_k} - e^{z_j} \cdot e^{z_i}}{(\sum_{k=1}^n e^{z_k})^2}$$

化简后：

$$\frac{\partial \sigma(z_j)}{\partial{z_i}} = - \frac{e^{z_j} \cdot e^{z_i}}{(\sum_{k=1}^n e^{z_k})^2} = -\sigma(z_j) \cdot \sigma(z_i)$$

到此为止$\frac{\partial \sigma (z_i)}{\partial z_i}$我们也求出来了。

最后求$\frac{\partial L}{\partial Z_i}$:

$$\frac{\partial L}{\partial z_i} = \frac{\partial L}{\partial \sigma (z_i)} \cdot \frac{\partial \sigma (z_i)}{\partial z_i} $$

这里还是分两种情况：

1.i = j 时：

$$\frac{\partial L}{\partial z_i} = \frac{\partial L}{\partial \sigma (z_i)} \cdot \frac{\partial \sigma (z_i)}{\partial z_i} = - \frac{y_i}{\sigma (z_i)} \cdot \frac{\sigma (z_i)(1-\sigma (z_i))}{1} = -y_i(1-\sigma (z_i))$$

由于$y_i$等于1，所以最后结果为$\sigma(z_i)-1$。

2.$i \neq j$时：

$$\frac{\partial L}{\partial z_i} = \frac{\partial L}{\partial \sigma (z_j)} \cdot \frac{\partial \sigma (z_j)}{\partial z_i} = - \frac{y_i}{\sigma (z_j)} \cdot \frac{-\sigma(z_j) \cdot \sigma(z_i)}{1} = \sigma(z_i)$$

将两种情况进行统一,可以看作是：

$$\frac{\partial L}{\partial z_i} = \sigma(z_i) - y_i = \widehat y - y$$

其中y是目标值，one-hot编码下，只有正确的类别为1，其余类表为0。以上公式用通俗的语言表示：

>输出层激活函数使用softmax，损失函数使用交叉熵函数时，输出层的误差梯度可以简化为$\widehat y - y$,也就是使用激活函数（softmax）后得到的值减去目标值。

## 总结

本小节讲解了偏导数，以及链式求导法则。其中使用softmax函数与交叉熵函数组合的复合函数求偏导有点难理解，大家可以多看几遍。