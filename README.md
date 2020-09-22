# 知识蒸馏
![](./img/knowledge-distillation.png)

<strong>知识蒸馏</strong>（a.k.a Teacher-Student Model)旨在利用一个小模型（Student）去学习一个大模型（Teacher）中的知识，
期望小模型尽量保持大模型的性能，来减小模型部署阶段的参数量，加速模型推理速度，降低计算资源使用。

# 目录结构
- 1.参考[Distilling the Knowledge in a Neural Network](http://arxiv.org/abs/1503.02531) (Hinton et al., 2015),
在cifar10数据上的复现，提供一个对Knowledge Distillation的基本认识，具体内容请查阅：[Knowledge_Distillation_From_Scratch.ipynb](Knowledge_Distillation_From_Scratch.ipynb)
- 2.利用BERT-12 作为Teacher，BERT-3作为student，同时学习ground truth 和 soften labels，性能与Teacher 相当甚至更优，具体内容请查阅：[knowledge_distillation_bert](https://github.com/xv44586/Knowledge-Distillation-NLP/knowledge_distillation_bert.py)
  
  主要参考论文：
  - [Distilling Task-Specific Knowledge from BERT into Simple Neural Networks](http://arxiv.org/abs/1903.12136) 
  - [TinyBERT: Distilling BERT for Natural Language Understanding](http://arxiv.org/abs/1909.10351)
  - [DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter](http://arxiv.org/abs/1910.01108)
  
- 3.利用模块替换的思路，来进行Knowledge Distillation，具体内容请查阅：[knowledge_distillation_bert_of_theseus](https://github.com/xv44586/Knowledge-Distillation-NLP/knowledge_distillation_bert_of_theseus.py)

   论文：
   - [BERT-of-Theseus: Compressing BERT by Progressive Module Replacing](http://arxiv.org/abs/2002.02925)
   
   Blog:
   - [BERT-of-Theseus：基于模块替换的模型压缩方法](https://spaces.ac.cn/archives/7575)
   - [模型压缩实践系列之——bert-of-theseus，一个非常亲民的bert压缩方法](https://zhuanlan.zhihu.com/p/112787764)
   
   repo:
   - [https://github.com/JetRunner/BERT-of-Theseus](https://github.com/JetRunner/BERT-of-Theseus)
   - [https://github.com/bojone/bert-of-theseus](https://github.com/bojone/bert-of-theseus)
   
 - 4.利用不同样本预测的难易程度不同，来动态选择模型的branch classifier，不过由于tensorflow1.X 是静态图，所以当前实现的
 demo实际上并不会真的提前结束计算，具体内容请查阅：[knowledge_distillation_fastbert](https://github.com/xv44586/Knowledge-Distillation-NLP/knowledge_distillation_fastbert.py)
 
 论文：
 - [FastBERT: a Self-distilling BERT with Adaptive Inference Time](http://arxiv.org/abs/2004.02178)