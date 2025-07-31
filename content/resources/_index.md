---
title: "资源共享"
description: "Datasets, Benchmarks and Tools from KILab"
---

我们致力于推动知识智能领域的开放研究，向学术界和产业界共享我们的数据集、基准测试和工具。

---

## 数据集 (Datasets)

### 知识图谱数据集

#### {{< icon "circle-info" >}} CN-Academic-KG
**中文学术知识图谱**

{{< figure src="/images/dataset_academic.png" alt="CN Academic Knowledge Graph" width="300" class="rounded" >}}

包含100万+中文学术实体和关系的大规模知识图谱，涵盖计算机科学、数学、物理等多个学科领域。

{{< button href="https://github.com/KILab/CN-Academic-KG" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/cn_academic_kg_2024.pdf" >}}{{< icon "pencil" >}} 论文{{< /button >}}

#### {{< icon "circle-info" >}} MultiModal-KG
**多模态知识图谱**

{{< figure src="/images/dataset_multimodal.png" alt="MultiModal Knowledge Graph" width="300" class="rounded" >}}

融合文本、图像和数值信息的多模态知识图谱，包含50万+实体和200万+三元组。

{{< button href="https://github.com/KILab/MultiModal-KG" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/multimodal_kg_2024.pdf" >}}{{< icon "pencil" >}} 论文{{< /button >}}

### 自然语言处理数据集

#### {{< icon "comment" >}} FewShot-RE-ZH
**中文少样本关系抽取**

{{< figure src="/images/dataset_fewshot.png" alt="Few-Shot Relation Extraction Dataset" width="300" class="rounded" >}}

专为中文少样本关系抽取设计的数据集，包含20个关系类别，每类仅有1-5个标注样本。

{{< button href="https://github.com/KILab/FewShot-RE-ZH" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/fewshot_re_2023.pdf" >}}{{< icon "pencil" >}} 论文{{< /button >}}

#### {{< icon "comment" >}} Dialogue-KG
**对话知识图谱**

{{< figure src="/images/dataset_dialogue.png" alt="Dialogue Knowledge Graph" width="300" class="rounded" >}}

基于真实对话构建的知识图谱，用于评估对话系统的知识推理能力。

{{< button href="https://github.com/KILab/Dialogue-KG" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/dialogue_kg_2023.pdf" >}}{{< icon "pencil" >}} 论文{{< /button >}}

---

## 基准测试 (Benchmarks)

### KG-Benchmark Suite

{{< figure src="/images/benchmark_overview.png" alt="KG Benchmark Suite" width="600" class="rounded" >}}

我们开发了一套综合的知识图谱基准测试套件，涵盖多个核心任务：

#### {{< icon "circle-info" >}} 实体链接 (Entity Linking)
- **数据集**: 5个领域，10万+标注样本  
- **评估指标**: Precision, Recall, F1-Score  
- **基线模型**: 10个SOTA模型对比

#### {{< icon "link" >}} 关系抽取 (Relation Extraction)
- **数据集**: 中英双语，50个关系类型  
- **评估指标**: Micro/Macro F1, AUC  
- **基线模型**: 15个经典和最新模型

#### {{< icon "lightbulb" >}} 知识推理 (Knowledge Reasoning)
- **数据集**: 多跳推理，复杂查询  
- **评估指标**: MRR, Hits@K  
- **基线模型**: 8个图神经网络模型

{{< button href="https://github.com/KILab/KG-Benchmark-Suite" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="https://benchmark.kilab.org" >}}{{< icon "globe" >}} 在线评估{{< /button >}}

---

## 开源工具 (Tools)

### KG-Toolkit

{{< alert "code-bracket" >}}
**一站式知识图谱工具包**  
集成了知识抽取、推理、可视化等功能的Python工具包
{{< /alert >}}

```python
# 安装
pip install kg-toolkit

# 使用示例
from kg_toolkit import KnowledgeGraph, EntityExtractor

# 创建知识图谱
kg = KnowledgeGraph()

# 实体抽取
extractor = EntityExtractor(model='bert-base-chinese')
entities = extractor.extract("张三是中山大学的教授")
```

**功能特性**:
- 🚀 多种预训练模型支持
- 📊 可视化知识图谱
- 🔧 灵活的API接口
- 📚 详细的文档和教程

{{< button href="https://github.com/KILab/KG-Toolkit" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="https://pypi.org/project/kg-toolkit/" >}}{{< icon "circle-info" >}} PyPI{{< /button >}}

### NLP-Utils

{{< alert "wrench-screwdriver" >}}
**自然语言处理工具集**  
包含文本预处理、特征提取、模型评估等实用功能
{{< /alert >}}

**主要模块**:
- 中文文本分词和词性标注
- 命名实体识别
- 关系抽取
- 文本分类
- 语义相似度计算

{{< button href="https://github.com/KILab/NLP-Utils" >}}{{< icon "github" >}} GitHub{{< /button >}}

---

## 教程和文档 (Tutorials)

### 入门教程

#### {{< icon "circle-info" >}} 知识图谱基础
适合初学者的知识图谱入门教程，包含理论基础和实践操作。
{{< button href="/tutorials/kg-basics" >}}开始学习{{< /button >}}

#### {{< icon "lightbulb" >}} 图神经网络实战
深入浅出地介绍图神经网络的原理和实现。
{{< button href="/tutorials/gnn-tutorial" >}}开始学习{{< /button >}}

#### {{< icon "translate" >}} NLP流水线
从数据预处理到模型部署的完整NLP项目教程。
{{< button href="/tutorials/nlp-pipeline" >}}开始学习{{< /button >}}

### 技术博客

定期更新技术博客，分享最新研究成果和技术见解：

- [知识图谱在推荐系统中的应用](./blog/kg-in-recommender-systems)
- [少样本学习最新进展](./blog/few-shot-learning-advances)
- [多模态AI的发展趋势](./blog/multimodal-ai-trends)

---

{{< alert "heart" >}}
**贡献指南**: 欢迎社区贡献代码、报告问题或提出改进建议！请查看各项目的 CONTRIBUTING.md 文件了解详情。
{{< /alert >}}

{{< alert "envelope" >}}
**联系我们**: 如需技术支持或合作，请发邮件至 [contact@kilab.org](mailto:contact@kilab.org)
{{< /alert >}}