# 【CV】常见术语及基本概念 in Mess

+ BND Box：即 Bounding Box，边界框。
+ GT：Ground Truth，表示检测任务希望检测出的矩形框（真实框），包括矩形框信息和类别信息。
+ DT：Detection Truth，表示模型检测出的矩形框（预测框），包括矩形框信息和类别信息。
+ Anchor：锚框。不同于边界框，Anchor是深度学习模型内部提前假定的框，用以框住需要检测的物体，以实现定位功能。Anchor 和先验框越匹配，训练效果越好。</br>通常会预先设定9个尺寸，也存在 Anchor-free （不需要 Anchor）的网络。

# 【CV】常见术语缩写

+ SR: 超分辨率重建（super-resolution reconstruction）
+ SISR：单图像超分辨率（single-image super-resolution）
+ MISR: 多图像超分辨率（multi-image super-resolution）