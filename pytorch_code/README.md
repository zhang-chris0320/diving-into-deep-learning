# 第三章起：纯 PyTorch 代码

这是《动手学深度学习（PyTorch 第二版）》从第 3 章到第 15 章的代码重写包。

## 改写原则

- 删除 `from d2l import torch as d2l` 及所有对 `d2l` 包的依赖。
- 张量、自动微分、网络层、损失函数、优化器和数据迭代器使用 PyTorch / torchvision。
- 将书中反复使用的绘图、计时、数据集下载和训练循环集中放在 `chapters/common.py`；这是本包自己的普通 Python 模块，不需要安装 d2l。
- 每个小节保留为一个 `.py` 文件；每章另有 `all_sections.py`，按书中目录顺序串联该章代码。
- 第 5 章“延后初始化”使用 PyTorch 原生 `nn.LazyLinear` 重写，因为上游多后端源码没有独立的 PyTorch 代码块。

## 目录

```text
chapters/
  common.py
  chapter_03_linear_networks/
  chapter_04_multilayer_perceptrons/
  ...
  chapter_15_nlp_applications/
manifest.json
```

`manifest.json` 给出每个输出文件对应的原书小节和代码块数量。

## 安装与运行

```bash
pip install -r requirements.txt
python chapters/chapter_03_linear_networks/linear_regression_scratch.py
```

也可以运行一整章：

```bash
python chapters/chapter_06_convolutional_neural_networks/all_sections.py
```

涉及 Fashion-MNIST、IMDb、SNLI、VOC、香蕉检测等示例时，程序会按需下载数据；完整训练可能需要 GPU 和较长时间。

## 来源与范围

代码结构按官方中文 2.0.0 源码和用户提供的 PDF 交叉核对，范围为第 3--15 章；第 16 章附录未纳入。官方项目的版本和许可证信息见 [d2l-ai/d2l-zh v2.0.0](https://github.com/d2l-ai/d2l-zh/releases/tag/v2.0.0)。
