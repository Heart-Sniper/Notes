# 常见术语及基本概念 in Mess

+ pretext task：即预训练任务，也称前置任务、代理任务。
+ downstream task：下游任务，通常指代对网络进行微调的任务。
+ end to end：端到端。提供一个输入，就得到一个输出。
+ backbone：指代主干网络。通常是负责提取特征的网络。
+ head：输出层。基于之前提取的特征，head 利用这些特征做出预测。
+ neck：指放在 backbone 和 head 之间的，为了更好地利用 backbone 提取的特征而进行相关处理的网络。
+ bottleneck：瓶颈。指网络的输入维度>>输出维度。</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;通常设置 bottle_num=256 ,指网络的输出维度为256。
+ baseline：作为基准的模型，用作比较模型效果的参考点。</br>
&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;baseline有助于模型开发者针对特定问题量化最低预期效果。
+ batch：模型训练时，一次迭代（即一次梯度更新）中使用的样本集。
+ batch size：一个 batch 中的样本数量。
+ bias：偏差，也称偏差项，代表距离原点的截距或偏移。</br>
&emsp;&emsp;&ensp;&thinsp;偏差在机器学习模型中通常用b或者w<sub>0</sub>表示。
+ binary classification：二元分类。
+ class-imbalanced：分类不平衡的。
+ checkpoint：检查点，一种数据，用于捕获模型变量在特定时间的状态。</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;借助 checkpoint，可以导出模型权重，跨多个会话执行训练，使模型在发生错误后得以继续（例如作业抢占）。</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&thinsp;注意：checkpoint 并不包含图（网络结构）本身。
+ cost：成本，近似于“损失”的含义。
+ clustering：聚类。
+ decision boundary：决策边界。在分类问题中，模型学到的类别之间的分界线。
+ dense feature：密集特征。一种大部分值是非零值的特征，通常是浮点值张量。</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;与稀疏特征相对。
+ discrete feature：离散特征，包含有限个可能值。</br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;&nbsp;与连续特征相对。
+ badcase：模型预测效果较差的样本/样本类型。
+ query：中文直译为“查询”，泛指请求或寻求系统、模型、数据集或数据库的特定信息、预测或操作。
  + 在神经网络中：query 通常是指“向模型提供输入以进行预测或推理”。模型基于该输入的输出被视为 query result。
  + 在Attention中：在基于Attention的模型（e.g. Transformer）中，query 是用于计算注意力权重时使用的键和值的三个组成部分之一。</br>query 用于根据键值计算注意力分数，以便从值中检索信息。
+ BND Box：即 Bounding Box，边界框。
+ GT：Ground Truth，表示检测任务希望检测出的矩形框（真实框），包括矩形框信息和类别信息。
+ DT：Detection Truth，表示模型检测出的矩形框（预测框），包括矩形框信息和类别信息。
+ Anchor：锚框。不同于边界框，Anchor是深度学习模型内部提前假定的框，用以框住需要检测的物体，以实现定位功能。Anchor和先验框越匹配，训练效果越好。</br>通常会预先设定9个尺寸，也存在 Anchor-free （不需要 Anchor）的网络。

# 常见术语缩写

+ SSLD：简单的半监督标签蒸馏法（Simple Semi-supervised Label Distillation） </br>
 &emsp;&emsp;&emsp;&thinsp;Paddlepaddle提供的一种知识蒸馏方案。
+ MSA：多头注意力机制（Multi-head Self-Attention）
+ FC：全连接层（Fully connected layer）
+ OHEM: 在线难例挖掘（Online hard example mining）
+ BN：批归一化（Batch Normalization）
+ GAP：全局平均池化（Global Average Pooling）
+ BP：反向传播（Back-propagation）