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

