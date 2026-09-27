# 动手学深度学习纯 PyTorch 版本

本仓库整理《动手学深度学习（PyTorch 第二版）》第 3—15 章的纯 PyTorch 代码，并配套一个按“大网络”划分的可视化网站。

## 内容

- `pytorch_code/`：按章节整理的 Python 源码，使用 PyTorch / torchvision，移除 `d2l` 命名空间依赖。
- `website/`：网络结构图谱网站，可按模块查看 LeNet、ResNet、RNN、Transformer、BERT、TextCNN、SSD 等网络。
- `docs/`：带中文注释、章节标注和结构图的 PDF 版代码手册。

## 快速开始

```bash
cd pytorch_code
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
```

每个章节目录中的 `all_sections.py` 汇总该章代码；也可以直接运行同目录下的单个示例文件。

## 网站本地预览

```bash
cd website/dist
python -m http.server 4173
```

然后打开 <http://127.0.0.1:4173/>。

## 在线网站

<https://zhang-chris0320.github.io/diving-into-deep-learning/>

网站通过 GitHub Pages 自动发布，不依赖 `chatgpt.site`。更新 `website/dist/` 后，GitHub Actions 会自动部署最新版本。

## 说明

本仓库不包含原书 PDF，仅整理代码、结构图和学习辅助材料。代码中的章节说明与示例来源于 D2L 中文 PyTorch 版本，使用时请遵守原书和相关项目的许可要求。
