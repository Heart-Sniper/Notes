# Roof-line Model

## Roof-line Model 研究什么问题

&emsp;&emsp;模型在一个计算平台的限制下，能达到多快的浮点计算速度。</br>

## Roof-line

&emsp;&emsp;Roof-line指的是由计算平台的算力和带宽上限这两个参数所决定的“屋顶”形态。</br>

<div align=center> 

![](Images\Roof-line.png)

</div>

按照Roof-line模型，模型的实际执行时间如下：
$$计算时间=\frac{计算量F}{计算速度}=\frac{计算量F}{min(\frac{计算量F}{访存量B}\times带宽\beta，理论算力\pi)}$$

## 访存密集型算子/计算密集型算子

神经网络中的算子可以根据计算强度进行分类。

+ 常见的计算密集型算子：Conv, FC, Deconv
+ 常见的访存密集型算子：ReLU, Concat

&emsp;&emsp;同一个算子也会因为参数的不同而导致计算密度变化，甚至改变性质。比如再其他参数不变的前提下，增大 Conv 的 group，或者减小 Conv 的 input channel 都会减小计算密度。</br>
&emsp;&emsp;面向推理性能设计网络结构时，应尽量采用经典结构。大部分框架会对这些结构进行图优化，能够有效减少计算量与访存量。（e.g. Conv->BN->ReLU 就会融合成一个算子，但 Conv->ReLU->BN 就无法直接融合BN层。）</br>
&emsp;&emsp;算子的参数尽量用常见的配置（e.g. Conv 尽量使用3 $\times$ 3），框架会对这些特殊参数做特定优化。</br>
&emsp;&emsp;CNN 网络的 channel 数量尽量选择8的倍数。很多框架的算子实现在这样的 channel 数下的实现效果更好。