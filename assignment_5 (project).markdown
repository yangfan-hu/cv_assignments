# 计算机视觉大作业要求：卷积神经网络（CNN）学习与实践 

## 一、 实验任务与要求 

### 1. 经典 LeNet-5 网络实现与手写数字识别 
* **数据集**：MNIST 手写数字数据集（包含 0-9 共十个数字，训练集 6 万样本，测试集 1 万样本）。
    * *下载地址*：[http://yann.lecun.com/exdb/mnist/index.html](http://yann.lecun.com/exdb/mnist/index.html) 
* **任务目标**：
    * 搭建最基本的卷积神经网络（CNN）LeNet-5。
    * 使用 6 万训练样本对 LeNet-5 进行模型训练。
    * 对 MNIST 的 1 万测试样本进行测试，统计并输出最终的识别率是多少 (Acc. > 97%)。 

### 2. 物体分类 CNN 实现 
* **数据集**：CIFAR-10 数据库。 
    * *下载地址*：[http://www.cs.utoronto.ca/~kriz/cifar.html](http://www.cs.utoronto.ca/~kriz/cifar.html) 
* **任务目标**：
    * 构建一个用于物体分类的卷积神经网络（CNN）。
    * 利用 CIFAR-10 数据集实现物体分类功能的完整训练与测试 (Acc. > 75%)。 

### 3. 开发工具与框架规范
* **框架选择**：可以直接调用 **PyTorch** 等常用的深度学习开发库。
    * *参考链接*：[PyTorch 官网](https://pytorch.org/) 
* **函数调用**：允许直接调用框架提供的各种构建函数（如卷积层、池化层、全连接层等）以及训练相关的接口（如损失函数、优化器）。 
* **核心禁令**：**不能直接读取或加载各种深度学习开发工具中已训练好的 CNN 网络结构与参数。**（必须独立完成模型的搭建与训练）

---

## 二、 提交形式与内容规范

大作业最终需打包提交，提交文件必须包含以下两部分核心内容：

### 1. 实验报告 (Report)
* **文件格式**：提交 **PDF** 格式电子文档。
* **命名规范**：建议命名为 `学号_姓名_CV_CNN.pdf`。
* **内容要求**：严格按照后文“实验报告撰写规范”进行编写，字迹/排版清晰，逻辑严密，图表数据完整。

### 2. 源代码 (Source Code)
* **包含内容**：应当包含实现 MNIST（LeNet-5）和 CIFAR-10 两个实验任务的所有核心代码，如网络结构定义文件、训练脚本、测试/评估脚本等。
* **代码规范**：
    * 代码应具备良好的可读性，包含必要的行内注释与说明。
    * 提供一份简短的 `README.md` 说明文件，注明运行环境（Python 及库版本）以及如何运行代码进行复现（如训练指令、测试指令）。
    * **严禁抄袭**，代码将进行查重检测。如有两份代码相同，分数两个人平分（如总分100，作业得分88，但是有两份相同，那么这两份报告得分都是44）

---

## 三、 实验报告撰写规范

大作业需提交一份详尽的实验报告，报告必须包含且不限于以下核心板块：

### 1. 摘要与引言
* 简述实验的背景、目的以及所使用的工具和数据集。

### 2. 网络架构设计
* **参数配置表**：详细给出所构建的 LeNet-5 以及物体分类网络的拓扑结构参数，包括但不限于：输入输出特征图尺寸（Size）、卷积核大小（Kernel Size）、步长（Stride）、通道数（Channels）以及激活函数的类型。
* **网络拓扑图**（可选）：建议绘制或附上网络数据流图。

### 3. 实验环境配置
* 详细说明具体的软硬件环境：
    * **硬件环境**：CPU 型号、GPU 型号（如适用）。 
    * **软件环境**：操作系统（Linux / Windows / Mac OS）、Python 版本及深度学习框架（PyTorch）的具体版本。 

### 4. 训练过程与超参数设置
* 真实记录并陈述实验中使用的核心超参数：
    * 学习率（Learning Rate）
    * 批大小（Batch Size）
    * 优化器选择（如 SGD, Adam 等）
    * 训练迭代轮数（Epochs / Iterations）

### 5. 实验结果与可视化（评分核心）
* **损失曲线图（Loss Curves）**：绘制并展现训练过程中 **Training Loss** 和 **Validation/Test Loss** 随迭代次数（Epochs/Iterations）变化的趋势图，并对收敛过程进行简要分析。
* **准确率曲线图（Accuracy Curves）**：绘制并展现 **Training Accuracy** 和 **Test Accuracy** 随迭代轮数的变化过程。
* **定量指标评价**：以表格形式清晰列出模型在 MNIST 和 CIFAR-10 测试集上最终达到的准确率（Top-1 Accuracy）。

### 6. 总结、调参体会与反思
* 阐述在实验过程中遇到的问题（如过拟合、欠拟合、梯度消失等）及对应的解决方法。
* 分享调整超参数（如调整学习率、改变 Batch Size）时，观察到的模型性能变化心得。

---

## 四、 经典参考论文与资源

在网络搭建与报告撰写时，可主动参考并引用以下计算机视觉领域的经典学术文献：

1. **LeNet-5 经典文献**：
   > Y. LeCun, L. Bottou, Y. Bengio, P. Haffner. *Gradient-based learning applied to document recognition.* Proceedings of the IEEE, 1998. 
2. **AlexNet 经典文献**：
   > A Krizhevsky, I Sutskever, GE Hinton. *ImageNet classification with deep convolutional neural networks.* NIPS 2012. 
3. **ResNet 经典文献**：
   > Kaiming He et al. *Deep Residual Learning for Image Recognition.* CVPR 2016.
