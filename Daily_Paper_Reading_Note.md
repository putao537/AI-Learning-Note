### 2022.06.01
- ERNIE-ViL: Knowledge Enhanced Vision-Language Representations through Scene Graphs (AAAI'21, [PDF](https://ojs.aaai.org/index.php/AAAI/article/view/16431))  
  作者设计了 Scene Graph Prediction 任务来进行预训练，具体做法为：给定一张图像与对应文本，随机遮盖掉部分检测区域以及由 Scene Graph Parser解析得到的场景图中的部分节点，要求模型预测被遮盖的节点。  
- Context-aware Scene Graph Generation with Seq2Seq Transformers (ICCV'21, [PDF](https://openaccess.thecvf.com/content/ICCV2021/papers/Lu_Context-Aware_Scene_Graph_Generation_With_Seq2Seq_Transformers_ICCV_2021_paper.pdf))  
  作者认为目前的 SGG 方法大多都是对于各个三元组并行进行独立预测，并没有考虑不同三元组之间的上下文信息（如：一个人与冲浪板 vs 一个人与冲浪板 with 这个人穿着鞋并且旁边的人在海滩上）。因此，作者利用 Seq2Seq 结构进行 sequential conditioning。  
- Calibrated Multi-label Classification with Label Correlations (Neural Processing Letters'19, [PDF](https://link.springer.com/content/pdf/10.1007/s11063-018-9925-2.pdf))  
  Authors introduce a label covariance matrix to characterize the label correlations and a virtual label to calibrate label decision threshold of each instance.  


### 2022.05.30
- Measuring Calibration in Deep Learning (CVPR Workshop'19, [PDF](https://openaccess.thecvf.com/content_CVPRW_2019/papers/Uncertainty%20and%20Robustness%20in%20Deep%20Visual%20Learning/Nixon_Measuring_Calibration_in_Deep_Learning_CVPRW_2019_paper.pdf))  
  作者讨论了 Expected Calibration Error 存在的问题，并提出 Adaptive Calibration Error (ACE)。
- Confidence Regularized Self-Training (ICCV'19, [PDF](https://openaccess.thecvf.com/content_ICCV_2019/papers/Zou_Confidence_Regularized_Self-Training_ICCV_2019_paper.pdf))  
  作者在 Unsupervised Domain Adaptation 问题中改进 Self-training 框架 (即模型生成伪标签以供模型不断迭代学习)，具体引入两种 Confidence Regularization (i.e., Label regularization and model regularization)。  
- Multivariate Confidence Calibration for Object Detection (CVPR Workshop'20, [PDF](https://openaccess.thecvf.com/content_CVPRW_2020/papers/w20/Kuppers_Multivariate_Confidence_Calibration_for_Object_Detection_CVPRW_2020_paper.pdf))  
  作者通过观察发现 "the calibration error depends on bounding box properties"，由此提出 Bbox-sensitive classification and regression branch based calibration method。   
- Beta calibration: a well-founded and easily implemented improvement on
logistic calibration for binary classifiers (PMLR'17, [PDF](http://proceedings.mlr.press/v54/kull17a/kull17a.pdf))  
  作者基于 Logistic Calibration 改进提出 Beta Calibration。
- Be Confident! Towards Trustworthy Graph Neural Networks via Confidence Calibration (NIPS'21, [PDF](https://openreview.net/pdf?id=9c-IsSptbmA))  
  作者通过观察发现图神经网络的置信度偏低，并且纠正后的图神经网络中邻居节点的置信度方差明显变小，由此提出 Learnable Topology Based Temperature Scaling Method。
  
### 2022.05.29
- On Calibration of Modern Neural Networks (ICML'17, [PDF](https://arxiv.org/abs/1706.04599))    
  作者提出模型的置信度纠正问题 (Confidence Calibration)，即模型所输出的置信度在不同区间内应具有与之相对应的准确率，以此符合我们对置信度的讨论意义。作者展示了多种衡量置信度与目标准确率差异的指标，如：Reliability Diagrams, Expected Calibration Error (ECE), Maximum Calibration Error (MCE), Negative log likelihood。此外，作者讨论了 Depth/Filters per layer/Batch Normalization/Weight decay 对置信度带来的影响。作者提出了 Temperature Scaling，即引入超参数 T 对置信度分布进行改变。值得注意的是，这是一种 Post-processing based calibration method，而且并不改变模型的准确率。    
- Bin-wise Temperature Scaling (BTS): Improvement in Confidence Calibration Performance through Simple Scaling Techniques (ICCV Workshop'19, [PDF](https://arxiv.org/pdf/1908.11528v2.pdf))  
  作者提出了 Bin-wise Temperature Scaling，即对于每个置信度区间引入一个超参数 T。  
- When Does Label Smoothing Help?  (NIPS'19, [PDF](https://arxiv.org/pdf/1906.02629.pdf))  
  作者主要讨论了 Label Smoothing 在深度学习中带来的好处与弊端。其中，Label Smoothing 可以起到置信度纠正的作用。  
- Trainable Calibration Measures For Neural Networks From Kernel Mean Embeddings (PMLR'18, [PDF](http://proceedings.mlr.press/v80/kumar18a/kumar18a.pdf))  
  作者基于 RKHS 引入 Maximum Mean Calibration Error (MMCE) 指标，以此在训练过程中约束模型的置信度。  
- Calibrating Deep Neural Networks using Focal Loss (NIPS'20, [PDF](https://arxiv.org/pdf/2002.09437.pdf))  
  作者讨论了 Focal Loss 之所以对于置信度纠正的有效的原因。  
