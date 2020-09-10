# 知识蒸馏
![](./img/knowledge-distillation.png)
知识蒸馏（a.k.a Teacher-Student Model)旨在利用一个小模型（Student）去学习一个大模型（Teacher）中的知识，
期望小模型尽量保持大模型的性能，来减小模型部署阶段的参数量，加速模型推理速度，降低计算资源使用。

# 目录结构
当前repo主要包括：
- 1.参考[Distilling the Knowledge in a Neural Network](http://arxiv.org/abs/1503.02531)( (Hinton et al., 2015)),
在cifar10数据上的简单复现，具体代码在[Knowledge_Distillation_From_Scratch.ipynb](Knowledge_Distillation_From_Scratch.ipynb)