MyCalculus
==================================

test1
---------------------------

中文
---------------------------

一元复合函数的求导法则
--------------------------

定理 1
```````````````
如果函数 :math:`u=g(x)` 在点 :math:`x` 可导，而函数 :math:`y=f(u)` 在对应点
:math:`u=g(x)` 可导，那么复合函数 :math:`y=f(g(x))` 在点 :math:`x` 可导，且有

.. math::
  \frac{\mathrm{d} y}{\mathrm{d} x}={f}'(u) \cdot {g}'(x) \quad  or \quad
  \frac{\mathrm{d} y}{\mathrm{d} x}=\frac{\mathrm{d} y}{\mathrm{d} u}\cdot \frac{\mathrm{d} u}{\mathrm{d} x}
  
严格来说函数 :math:`y=f(u)` 实际上只是 :math:`u` 的函数，并不是 :math:`x` 的函数。
而 :math:`h(x)=(f\circ g)(x)` 才是 :math:`x` 的函数。这种记号上的随意会在复杂问题上造成困扰。


.. math::
  \begin{align}
    \cfrac{h(x+\triangle x)-h(x)}{\triangle x } &=\cfrac{f(g(x+\triangle x))-f(g(x))}{\triangle x }\\
    &=\cfrac{[f(g(x+\triangle x))-f(g(x))]}{[g(x+\triangle x)-g(x)]}\cfrac{[g(x+\triangle x)-g(x)]}{\triangle x }
  \end{align}
  
.. math::
  \begin{align}
    \lim_{\triangle x \to 0}\cfrac{h(x+\triangle x)-h(x)}{\triangle x } &=\lim_{\triangle x \to 0}\cfrac{f(g(x+\triangle x))-f(g(x))}{\triangle x }\\
    &=\lim_{\triangle x \to 0}\cfrac{[f(g(x+\triangle x))-f(g(x))]}{[g(x+\triangle x)-g(x)]}\cfrac{[g(x+\triangle x)-g(x)]}{\triangle x }\\
    &=\frac{\mathrm{d} f(u)}{\mathrm{d} u} \Bigg|_{u=g(x)} \cdot \frac{\mathrm{d} g(x)}{\mathrm{d} x} \Bigg|_{x=x} 
  \end{align}

也就是说，如果把函数 :math:`y` 定义成 :math:`y=f(u)` ，那么复合函数就不要记作 :math:`y` ，这有歧义。这里不妨记作 :math:`h` ,
一般来说，:math:`h` 和 :math:`f` 的表达式显然不是一回事，这是两个不同的函数。
一般有：

.. math::
  \begin{align}
    y_{0}=f(u_{0})= f(u(x_{0} ))=  f(u(x ))\Bigg|_{x=x_{0}} 
  \end{align}
  
举个例子：

.. math::
  \begin{align}
    y(u)=f(u)=2u\\
    u(x)=g(x)=sin(x)\\
    h(x)=f(g(x))=(f \circ g)(x)=2sin(x)
  \end{align}
  
显然，这里的函数 :math:`y` 和 函数 :math:`h` 不是一回事。
我们可以将变量换为任何记号，比如 :math:`y(u)=f(u)=2u` 或者 :math:`y(t)=f(t)=2t` 或者 :math:`y(x)=f(x)=2x`
对于函数 :math:`h` 有 :math:`h(x)=2sin(x)` ,如果此时也记做 :math:`y(x)=2sin(x)` 则会造成歧义。

.. math::
  \begin{align}
    y(u)=f(u)=2u\\
    u(x)=g(x)=sin(x)\\
   \hat{y}(x)=h(x)=f(g(x))=(f \circ g)(x)=2sin(x)
  \end{align}
  
这里的函数 :math:`y` 和 函数 :math:`\hat{y}` 应该加以区分。

.. math::
  y(sin(x))=f(sin(x))=\hat{y}(x)=2sin(x)

从这个角度来说，定理更合理的表述应该是：

如果函数 :math:`u=g(x)` 在点 :math:`x` 可导，而函数 :math:`y=f(u)` 在对应点
:math:`u=g(x)` 可导，那么复合函数 :math:`\hat{y}=f(g(x))` 在点 :math:`x` 可导，且有

.. math::
  \frac{\mathrm{d} \hat{y}(x)}{\mathrm{d} x}={f}'(u) \cdot {g}'(x) \quad  or \quad
  \frac{\mathrm{d} \hat{y}(x)}{\mathrm{d} x}=\frac{\mathrm{d} y(u)}{\mathrm{d} u}\cdot \frac{\mathrm{d} u(x)}{\mathrm{d} x}

