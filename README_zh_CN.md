# ***NeuronBlocks*** - 像搭积木一样构建自然语言理解深度学习模型

* [概览](#概览)
* [适用人群](#适用人群)
* [快速入门](#快速入门)
* [参与贡献](#参与贡献)
* [参考文献](#参考文献)
* [相关项目](#相关项目)
* [License](#License) 
* [联系我们](#联系我们)



# 概览
NeuronBlocks是基于PyTorch的NLP深度学习建模工具包，可以帮助工程师们构建用于NLP任务的神经网络模型训练的端到端管道。
该工具包的主要目标是将NLP中深度神经网络模型构建的开发成本降到最低，包括训练阶段和推断阶段。
更多细节，请查看论文[NeuronBlocks -- Building Your NLP DNN Models Like Playing Lego](https://arxiv.org/abs/1904.09535).

NeuronBlocks包括Block Zoo和Model Zoo两个重要组件，其整体框架如下图所示。
- 在 ***Block Zoo*** 中, 我们提供了常用的神经网络组件作为模型架构设计的构建模块。
- 在 ***Model Zoo*** 中, 我们提供了 **JSON配置文件** 形式的一系列经典NLP深度学习模型。
 
<img src="https://i.imgur.com/LMD0PFQ.png" width="300">

### 使用方法

用户可以选择Model Zoo中的示例模型（JSON配置文件）开启模型训练，或者利用Block Zoo中的神经网络模块构建新的模型，就像玩乐高积木一样。

<img src="https://i.imgur.com/q0p6Wvz.png" width="300">


### 支持的NLP任务
- 句子分类
- 问答匹配
- 文本蕴含
- 序列标注
- 阅读理解
- 更多……

# 适用人群
在用神经网络模型解决NLP任务时面临以下挑战的工程师和研究者们：
+ 很多框架可以选择，且框架学习成本高；
+ 繁重的编程工作，大量细节使其难以调试；
+ 快速迭代的模型架构，使工程师们很难完全理解其背后的数学原理；
+ 模型代码优化需要深厚的专业知识；
+ 平台兼容性要求，需要额外的编程工作才能使模型运行在不同的平台上，如Linux/Windows, GPU/CPU。

利用NeuronBlocks进行NLP神经网络模型训练的优势包括：
- ***模型构建***：用户只需要配置简单的JSON文件，就能够构建模型和调整参数，大大减少了模型实现的工作量；
- ***模型分享***：可以通过分享JSON配置文件来分享模型，使模型共享变得非常容易。对于不同的任务或模型，用户只需维护一个通用的源码库；；
- ***代码重用***：可以在各任务与模型间共享神经网络模块，减少重复的编程工作；；
- ***平台灵活性***：NeuronBlocks可以在Linux和Windows机器上运行，支持CPU和GPU，也支持像Philly和PAI这样的GPU管理平台；；
- ***模型可视化***：NeuronBlocks提供了一个模型可视化工具，用于观察模型结构及检查JSON配置的正确性；；
- ***可扩展性***：NeuronBlocks鼓励用户贡献新的神经网络模块或着新的模型。

# 快速入门
## 安装

*注: NeuronBlocks支持Python 3.6*

1. Clone本项目： 
    ```bash
    git clone https://github.com/Microsoft/NeuronBlocks
    ```

2. 安装Python依赖包：
    ```bash
    pip install -r requirements.txt
    ```

3. 安装PyTorch (*NeuronBlocks支持PyTorch 0.4.1*).
    
    对于 **Linux**，运行以下命令：
    ```bash
    pip install torch==0.4.1
    ```
    对于**Windows**，建议按照[PyTorch官方安装教程](https://pytorch.org/get-started/previous-versions/)通过Conda安装PyTorch。
    

## 快速开始

通过以下示例快速入门NeuronBlocks
Get started by trying the given examples.

*提示: 在下文中, PROJECTROOT表示本项目的根目录.*

```bash
# 训练
cd PROJECT_ROOT
python train.py --conf_path=model_zoo/demo/conf.json

# 测试
python test.py --conf_path=model_zoo/demo/conf.json

# 预测
python predict.py --conf_path=model_zoo/demo/conf.json
```

更多细节, 请查看[Tutorial.md](Tutorial.md)和[Code documentation](https://microsoft.github.io/NeuronBlocks/).

# 参与贡献
NeuronBlocks以开放的模式运行。它由**Microsoft STCA NLP Group**设计和开发，也非常欢迎来自学术界和工业界的人士参与贡献。更多详细信息，请查看[Contributing.md](Contributing.md)。

## 正在进行的工作
* 模型压缩，对诸如BERT, OpenAI Transformer之类的重型模型进行知识蒸馏。基于Teacher-Student的知识蒸馏是模型压缩的一个常用方法。
* 多语言支持
* 命名实体识别模型支持
* 多任务训练支持

# 参考文献
[**NeuronBlocks -- Building Your NLP DNN Models Like Playing Lego**](https://arxiv.org/abs/1904.09535).

# 相关项目
* [OpenPAI](https://github.com/Microsoft/pai): 作为开源平台，提供了完整的 AI 模型训练和资源管理能力，能轻松扩展，并支持各种规模的私有部署、云和混合环境。
* [Samples for AI](https://github.com/Microsoft/samples-for-ai): 一个深度学习样例与项目集合。它包括大量基于不同框架的经典深度学习算法和应用，对于初学者来说是很好的入门深度学习的工具。

# License

Copyright (c) Microsoft Corporation. All rights reserved.

Licensed under the [MIT](LICENSE) License.

# 联系我们
如有任何问题，请联系：NeuronBlocks@microsoft.com