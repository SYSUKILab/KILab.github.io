---
title: "Resources"
description: "Research Projects, Datasets, Benchmarks and Tools from KILab"
cascade:
    showSummary: true
---

We are committed to promoting open research in the field of knowledge intelligence, sharing our research projects, datasets, benchmarks, and tools with the academic and industrial communities.

---

## Research Projects

Our research focuses on cutting-edge fields including trustworthy artificial intelligence, intelligent information retrieval, natural language processing, and knowledge intelligence applications, committed to promoting the deep integration of theoretical innovation and practical applications.

### {{< icon "check" >}} AI Security and Trust

In today's rapidly evolving AI landscape, ensuring the security and trustworthiness of AI systems is crucial. We conduct in-depth research in this frontier field:

**Core Research Areas:**
- **Trustworthy AI Algorithms**: Design AI algorithms with robustness, explainability, and fairness
- **AIGC Security**: Research on security risks and protection mechanisms for AI-generated content
- **AI Model Reliability**: Enhance the stability of deep learning models under adversarial attacks
- **Privacy-Preserving AI**: Develop federated learning and differential privacy technologies to protect user privacy

### {{< icon "search" >}} Intelligent Information Retrieval

Information retrieval is the key technology connecting user needs with massive information. We focus on personalized and intelligent information retrieval system research:

**Core Research Areas:**
- **Recommendation Systems**: Deep learning-based personalized recommendation algorithms
- **User Modeling and Understanding**: Multi-dimensional user profiling and behavior prediction
- **Knowledge Acquisition**: Automatic acquisition of structured knowledge from multi-source heterogeneous data
- **Search Technologies**: Next-generation intelligent search engine technologies

### {{< icon "comment" >}} Natural Language Processing

Natural language processing is the core technology for achieving intelligent human-machine interaction. We conduct cutting-edge research in large-scale language models and multimodal understanding:

**Core Research Areas:**
- **Large Language Models (LLM)**: Optimization and application of pre-trained models
- **Multimodal Knowledge Extraction**: Knowledge extraction fusing visual and linguistic information
- **Knowledge Representation Learning**: Vectorized representation and reasoning of textual knowledge
- **Dialogue Systems**: Knowledge-driven intelligent dialogue technologies

### {{< icon "globe" >}} Spatial-Temporal Analysis and Prediction

Spatial-temporal data analysis has important application value in intelligent transportation, urban computing, and other fields:

**Core Research Areas:**
- **Location-aware Social Network Analysis**: Geographic location-based social behavior modeling
- **Real-time Push Algorithms**: Spatial-temporal aware information push systems
- **Traffic Data Analysis**: Data mining and prediction for intelligent transportation systems
- **Time Series Prediction**: Deep learning prediction models for multivariate time series

### {{< icon "lightbulb" >}} Knowledge Intelligence Applications

Apply knowledge intelligence technologies to real industry scenarios, solving complex real-world problems:

**Core Research Areas:**
- **Intelligent Finance**: Knowledge graph-based financial risk control and investment decision-making
- **Intelligent Transportation**: Traffic flow optimization and intelligent navigation systems
- **Recommendation System Applications**: Industrial applications in e-commerce, content recommendation, and other fields
- **Multimedia Content Understanding**: Intelligent analysis and understanding of videos and images

{{< alert "light-bulb" >}}
**Research Project Support**: The laboratory leads multiple important research projects including National Natural Science Foundation, Guangdong Natural Science Foundation, CCF-DiDi GAIA Young Scholar Program, and others.
{{< /alert >}}

---

## Datasets

### Knowledge Graph Datasets

#### {{< icon "circle-info" >}} CN-Academic-KG
**Chinese Academic Knowledge Graph**

{{< figure src="/images/dataset_academic.png" alt="CN Academic Knowledge Graph" width="300" class="rounded" >}}

A large-scale knowledge graph containing over 1 million Chinese academic entities and relationships, covering multiple disciplines including computer science, mathematics, and physics.

{{< button href="https://github.com/KILab/CN-Academic-KG" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/cn_academic_kg_2024.pdf" >}}{{< icon "pencil" >}} Paper{{< /button >}}

#### {{< icon "circle-info" >}} MultiModal-KG
**Multimodal Knowledge Graph**

{{< figure src="/images/dataset_multimodal.png" alt="MultiModal Knowledge Graph" width="300" class="rounded" >}}

A multimodal knowledge graph that integrates textual, visual, and numerical information, containing over 500K entities and 2M+ triples.

{{< button href="https://github.com/KILab/MultiModal-KG" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/multimodal_kg_2024.pdf" >}}{{< icon "pencil" >}} Paper{{< /button >}}

### Natural Language Processing Datasets

#### {{< icon "comment" >}} FewShot-RE-ZH
**Chinese Few-Shot Relation Extraction**

{{< figure src="/images/dataset_fewshot.png" alt="Few-Shot Relation Extraction Dataset" width="300" class="rounded" >}}

A dataset specifically designed for Chinese few-shot relation extraction, containing 20 relation categories with only 1-5 annotated samples per category.

{{< button href="https://github.com/KILab/FewShot-RE-ZH" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/fewshot_re_2023.pdf" >}}{{< icon "pencil" >}} Paper{{< /button >}}

#### {{< icon "comment" >}} Dialogue-KG
**Dialogue Knowledge Graph**

{{< figure src="/images/dataset_dialogue.png" alt="Dialogue Knowledge Graph" width="300" class="rounded" >}}

A knowledge graph built from real dialogues, used to evaluate the knowledge reasoning capabilities of dialogue systems.

{{< button href="https://github.com/KILab/Dialogue-KG" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="/papers/dialogue_kg_2023.pdf" >}}{{< icon "pencil" >}} Paper{{< /button >}}

---

## Benchmarks

### KG-Benchmark Suite

{{< figure src="/images/benchmark_overview.png" alt="KG Benchmark Suite" width="600" class="rounded" >}}

We have developed a comprehensive knowledge graph benchmark suite covering multiple core tasks:

#### {{< icon "circle-info" >}} Entity Linking
- **Dataset**: 5 domains, 100K+ annotated samples  
- **Evaluation Metrics**: Precision, Recall, F1-Score  
- **Baseline Models**: 10 SOTA model comparisons

#### {{< icon "link" >}} Relation Extraction
- **Dataset**: Bilingual (Chinese-English), 50 relation types  
- **Evaluation Metrics**: Micro/Macro F1, AUC  
- **Baseline Models**: 15 classic and state-of-the-art models

#### {{< icon "lightbulb" >}} Knowledge Reasoning
- **Dataset**: Multi-hop reasoning, complex queries  
- **Evaluation Metrics**: MRR, Hits@K  
- **Baseline Models**: 8 graph neural network models

{{< button href="https://github.com/KILab/KG-Benchmark-Suite" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="https://benchmark.kilab.org" >}}{{< icon "globe" >}} Online Evaluation{{< /button >}}

---

## Open Source Tools

### KG-Toolkit

{{< alert "code-bracket" >}}
**All-in-One Knowledge Graph Toolkit**  
A Python toolkit that integrates knowledge extraction, reasoning, and visualization capabilities
{{< /alert >}}

```python
# Installation
pip install kg-toolkit

# Usage Example
from kg_toolkit import KnowledgeGraph, EntityExtractor

# Create knowledge graph
kg = KnowledgeGraph()

# Entity extraction
extractor = EntityExtractor(model='bert-base-chinese')
entities = extractor.extract("Zhang San is a professor at Sun Yat-sen University")
```

**Key Features**:
- 🚀 Multiple pre-trained model support
- 📊 Knowledge graph visualization
- 🔧 Flexible API interface
- 📚 Detailed documentation and tutorials

{{< button href="https://github.com/KILab/KG-Toolkit" >}}{{< icon "github" >}} GitHub{{< /button >}} 
{{< button href="https://pypi.org/project/kg-toolkit/" >}}{{< icon "circle-info" >}} PyPI{{< /button >}}

### NLP-Utils

{{< alert "wrench-screwdriver" >}}
**Natural Language Processing Utilities**  
Contains practical functions for text preprocessing, feature extraction, and model evaluation
{{< /alert >}}

**Main Modules**:
- Chinese text segmentation and POS tagging
- Named entity recognition
- Relation extraction
- Text classification
- Semantic similarity computation

{{< button href="https://github.com/KILab/NLP-Utils" >}}{{< icon "github" >}} GitHub{{< /button >}}

---

## Tutorials and Documentation

### Getting Started Tutorials

#### {{< icon "circle-info" >}} Knowledge Graph Fundamentals
A beginner-friendly knowledge graph tutorial covering theoretical foundations and practical operations.
{{< button href="/tutorials/kg-basics" >}}Start Learning{{< /button >}}

#### {{< icon "lightbulb" >}} Graph Neural Networks in Practice
An accessible introduction to the principles and implementation of graph neural networks.
{{< button href="/tutorials/gnn-tutorial" >}}Start Learning{{< /button >}}

#### {{< icon "translate" >}} NLP Pipeline
A complete NLP project tutorial from data preprocessing to model deployment.
{{< button href="/tutorials/nlp-pipeline" >}}Start Learning{{< /button >}}

### Technical Blog

Regularly updated technical blog sharing latest research findings and technical insights:

- [Applications of Knowledge Graphs in Recommender Systems](./blog/kg-in-recommender-systems)
- [Recent Advances in Few-Shot Learning](./blog/few-shot-learning-advances)
- [Development Trends in Multimodal AI](./blog/multimodal-ai-trends)

---

{{< alert "heart" >}}
**Contribution Guidelines**: We welcome community contributions including code, issue reports, and improvement suggestions! Please check the CONTRIBUTING.md file in each project for details.
{{< /alert >}}

{{< alert "envelope" >}}
**Contact Us**: For technical support or collaboration, please email [contact@kilab.org](mailto:contact@kilab.org)
{{< /alert >}}