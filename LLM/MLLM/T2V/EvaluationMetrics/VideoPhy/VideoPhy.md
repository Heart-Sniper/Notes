# VideoPhy: Evaluating Physical Commonsense for Video Generation

## 研究目的

旨在评估文本生成视频模型在物理常识方面表现。

## 研究背景

现有的T2V模型严重缺乏`准确拟合caption`和`生成具有物理常识的视频`的能力。

## 相关研究

+ Fréchet video distance (FVD): Fréchet 视频距离（FVD）传统上用于测量真实视频分布与生成视频分布之间的相似性。然而，FVD 在评估物理常识方面有一些局限性，包括需要参考视频（新场景很难获得参考视频）、偏向视频质量以及无法检测到不真实的运动。
+ ClIP Score: CLIP Score 在共享表示空间中测量生成视频帧与条件文本之间的语义相似性，因此不适合评估生成视频中的物理常识。

## 研究过程

## VIDEOPHY Dataset

### 数据集构建方法

  1. 通过对 LLM 进行 prompt， 使 LLM 生成描述视频中不同物质状态（如：固体-固体，固体-流体，流体-流体）的候选 caption；
  2. 对候选 caption 进行人工验证；
  3. 对 caption 中描述的物体或运动的复杂性进行注释；
  4. 根据注释好的 prompt，利用现有的 9 个 T2V 模型来生成视频。
 