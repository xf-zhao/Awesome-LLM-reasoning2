# Awesome LLM reasoning

<!-- <div style="text-align: center;">

    <h1><img src="assets/logo.png" height="28px" /> Awesome-LLM-reasoning </h1>

</div> -->



[![Awesome](https://awesome.re/badge.svg)](https://github.com/luban-agi/Awesome-LLM-reasoning) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
![](https://img.shields.io/badge/PRs-Welcome-red)
<!---![](https://img.shields.io/github/last-commit/luban-agi/Awesome-LLM-reasoning) -->


Awesome papers on LLM reasoning.

## 📜 Table of Contents

- [📚 Papers](#-papers)
  
  - [🌟 Graph of Thought](#-graph-of-thought)
  - [📌 Backward Reasoning ](#-backward-reasoning)
    - [Backward Chaining](#backward-chaining)
    - [Question Decomposition](#question-decomposition)
  - [💪 Reasoning Enhancement for Small LM ](#-reasoning-enhancement-for-small-lm)
    - [Distillation](#distillation)
    - [Step-aware Reasoning](#step-aware-reasoning)
    - [Self-Training](#self-training)
  - [📑 Survey](#-survey)
<!--- [📱 Applications](#-applications)  -->
<!--- [🎉 Contributors](#-contributors) -->

## 📚 Papers

### 🌟 Graph of Thought
- **Beyond Chain-of-Thought, Effective Graph-of-Thought Reasoning in Large Language Models**, 2023.05 <br />
*Yao Yao, Zuchao Li, Hai Zhao* [[abs](https://arxiv.org/abs/2305.16582)]
    - <p align = "center">   <img src="https://github.com/luban-agi/Awesome-LLM-reasoning/assets/22321904/95a68e1f-d036-4537-af09-b19b02fecd1e" width="700" />     </p>
    - *This paper proposes a method for Graph of Thoughts (GOT) that focuses on the construction of graph-strucuture data. Specifically, the method employed in this study is Structure-Aware Abstractive Conversation Summarization via Discourse and Action Graphs. The central idea of this paper is to transform the rationale into graph format using the preceding context. However, I believe this approach does not truly embody the essence of GOT, as each node does not represent a distinct thinking step but rather converts the natural language prompt into a graph format. Additionally, the motivation behind this paper is not adequately explained. Although the concept of multimodality is introduced in the study, I do not perceive it as the crux of the GOT problem.*
   

 
- **Thinking Like an Expert:Multimodal Hypergraph-of-Thought (HoT) Reasoning to boost Foundation Modals**, 2023.08 <br />
*Fanglong Yao, Changyuan Tian, Jintao Liu, Zequn Zhang, Qing Liu, Li Jin, Shuchao Li, Xiaoyu Li, Xian Sun* [[abs](https://arxiv.org/abs/2308.06207)]
    - <p align = "center">        <img src="https://github.com/luban-agi/Awesome-LLM-reasoning/assets/22321904/58afc313-2666-402e-8e7a-855e92cde038" width="700" />     </p>
    - *Similar to "Beyond Chain-of-Thought, Effective Graph-of-Thought Reasoning in Large Language Models," this paper presents a method for Graph of Thoughts (GOT) by transforming natural language prompts into a graph format. The key distinction lies in the utilization of hypergraphs for data modeling instead of conventional graphs. Personal opinion: 1) There is a similar issue as the previous paper, and I personally do not fully agree that a graph-structured prompt represents a true Graph of Thoughts (GOT). Although the perspective presented in this paper can be considered as one viewpoint, my ideal GOT would resemble human-like free thinking. 2) It is not very clear why there is a necessity to utilize hypergraphs for data modeling. The motivation behind this paper seems somewhat vague.*
    

- **Graph of Thoughts: Solving Elaborate Problems with Large Language Models**, 2023.08 <br />
*Maciej Besta, Nils Blach, Ales Kubicek, Robert Gerstenberger, Lukas Gianinazzi, Joanna Gajda, Tomasz Lehmann, Michal Podstawski, Hubert Niewiadomski, Piotr Nyczyk, Torsten Hoefler* [[abs](https://arxiv.org/abs/2308.09687)]
  - <p align = "center">        <img src="https://github.com/luban-agi/Awesome-LLM-reasoning/assets/22321904/e34146bd-cf1d-4732-b5fc-589a3b82488e" width="500" />     </p>
  - The core idea of this paper is to define how to construct a graph-structured chain of thoughts. It also introduces the concept of Graph of Operations (GoO), which includes operations such as generate (1-to-many), aggregate (many-to-1), and improve (self-improvement). Each step of reasoning requires the formulation of prompt through instructions and examples.
  - The proposed approach in this paper is comprehensive, and the writing is well-done. However, there are several issues:
    - The entire graph is static and predefined.
    - It relies on a well-defined scoring function, which is heavily task-dependent.
    - The paper does not elaborate on how to delete nodes. Although a definition is provided, the actual execution does not consider node deletion. This aligns with the first point, as the graph structure is predefined, and node deletion was not considered during the design phase
    

- **Boosting Logical Reasoning in Large Language Models through a New Framework: The Graph of Thought** 2023.08 <br />
*Bin Lei, pei-Hung Lin, Chunhua Liao, Caiwen Ding* [[abs](https://arxiv.org/abs/2308.08614)]
    - <p align = "center">        <img src="https://github.com/luban-agi/Awesome-LLM-reasoning/assets/22321904/01231678-6d72-4aa6-963b-f3e4983975b5" width="500" />     </p>
    - Similar to the previous paper, this article also demonstrates a well-presented motivation and proposes its own Graph of Thoughts (GOT) approach. However, it seems that this paper has omitted several details, particularly regarding the many-to-one reasoning process. The exact procedure for achieving many-to-one reasoning is not clearly explained.
The core ideas of this paper are as follows:
        - Starting from the desired results and backward reasoning to the condition nodes (with some doubts, as evidenced by the example of "Solving High-Degree Polynomial Equations").
        - Conducting reasoning by first using the Large Language Model (LLM) to calculate paths (resembling actions), and then obtaining new nodes based on the paths and LLM. However, the description provided in this regard is highly unclear, lacking a clear understanding of the specific procedure. As a reviewer, I would likely reject the paper based on this lack of clarity.
        - Introducing a validator (which can utilize LLM) as an additional component to verify the correctness of the paths.
    - The paper does not explain the details of the many-to-one reasoning process, which I consider to be the crux of the approach. In the experimental section, the paper reports promising results, surpassing those of the previous approach(TOT).

- **MindMap: Knowledge Graph Prompting Sparks Graph of Thoughts in Large Language Models** 2023.08 <br />
*Yilin Wen, Zifeng Wang, Jimeng Sun* [[abs](https://arxiv.org/abs/2308.09729)]
    - <p align = "center">        <img src="https://github.com/luban-agi/Awesome-LLM-reasoning/assets/22321904/76575179-56b4-4be1-bbd5-7fc3dd7be0ce" width="500" />     </p>
    - This article does not precisely align with my envisioned concept of Graph of Thoughts (GOT), which involves free thinking similar to human cognition. Instead, it focuses on reasoning with knowledge graphs (KG) or reasoning on graphs. Nevertheless, I believe that this work is solid, as it enables large-scale models to engage in systematic reasoning on graphs/KGs, which is an intriguing pursuit.
    - Key points: 
        - The utilization of knowledge graphs is a fundamental aspect of this approach.
        - The research is focused on specific domains, such as medical question answering, where precision in reasoning is paramount, and knowledge graphs provide substantial assistance.
        - The transformation of knowledge graph information into natural language is a notable contribution.
    - Specific steps:
        - Entity extraction from the given question, followed by querying subgraphs in the knowledge graph based on these entities.
        - Integration of multiple subgraphs into a comprehensive graph.
        - Transformation of the constructed graph into natural language form, along with the input question, to create a well-formed prompt that facilitates reasoning along the paths of the graph.


### 💡 With Graph
- **Structure-Aware Abstractive Conversation Summarization via Discourse and Action Graphs** 2021.04 <br />
*Jiaao Chen, Diyi Yang* [[abs](https://arxiv.org/abs/2308.06207)]

    - <p align = "center">   <img src="https://github.com/luban-agi/Awesome-LLM-reasoning/assets/22321904/b68240fb-2d55-4664-b3ec-9752f7e797ed" width="400" />     </p>
    - This article is quite interesting, although it is from 2021, which may be considered early. However, the motivation behind the research is clearly presented. The core idea is to augment text data with two types of graph structures to assist the model in understanding semantics. The paper "Beyond Chain-of-Thought, Effective Graph-of-Thought Reasoning in Large Language Models" draws inspiration from the approach proposed in this article.
    - In graph (a), the relationships between sentences in the dialogue are constructed, forming a so-called discourse parsing model. The edges between each pair of nodes represent a classification problem. Specifically, as stated in the paper, "We first pre-train a discourse parsing model (Shi and Huang, 2019) on a human annotated multiparty dialogue corpus (Asher et al., 2016), with 0.775 F1 score on link predictions and 0.557 F1 score on relation classifications."  Graph (b) adopts open information extraction (OpenIE) systems, specifically the implementation from https://github.com/philipperemy/Stanford-OpenIE-Python, to construct a simpler graph. Graph convolutional methods, such as Graph Attention Network, are employed for information extraction from both graphs.
    

### 📌 Backward Reasoning 
#### Backward Chaining
- **METGEN: A module-based entailment tree generation framework for answer explanation** 2022.05 <br />
*Ruixin Hong, Hongming Zhang, Xintong Yu, Changshui Zhang* [[abs](https://arxiv.org/abs/2205.02593)]

- **LAMBADA: backward chaining for automated reasoning in natural language** 2022.12 <br />
*Mehran Kazemi, Najoung Kim, Deepti Bhatia, Xin Xu, Deepak Ramachandran* [[abs](https://arxiv.org/abs/2212.13894)]

- **Entailer: Answering questions with faithful and truthful chains of reasoning** 2022.10 <br />
*Oyvind Tafjord, Bhavana Dalvi Mishra, Peter Clark* [[abs](https://arxiv.org/abs/2210.12217)]

- **Interpretable proof generation via iterative backward reasoning** 2022.05 <br />
*Hanhao Qu, Yu Cao, Jun Gao, Liang Ding, Ruifeng Xu* [[abs](https://arxiv.org/abs/2205.10714)]

#### Question Decomposition
- **Multi-hop Reading Comprehension through Question Decomposition and Rescoring** 2019.06 <br />
*Sewon Min, Victor Zhong, Luke Zettlemoyer, Hannaneh Hajishirzi* [[abs](https://arxiv.org/abs/1906.02916)]

- **Is a question decomposition unit all we need** 2022.05 <br />
*Pruthvi Patel, Swaroop Mishra, Mihir Parmar, Chitta Baral* [[abs](https://arxiv.org/abs/2205.12538)]

- **Unsupervised question decomposition for question answering** 2020.02 <br />
*Ethan Perez, Patrick Lewis, Wen-tau Yih, Kyunghyun Cho, Douwe Kiela* [[abs](https://arxiv.org/abs/2002.09758)]

- **Text modular networks: Learning to decompose tasks in the language of existing models** 2021.04 <br />
*Tushar Khot, Daniel Khashabi, Kyle Richardson, Peter Clark, Ashish Sabharwal* [[abs](https://arxiv.org/abs/2009.00751)]

- **Measuring and narrowing the compositionality gap in language models** 2022.10 <br />
*Ofir Press, Muru Zhang, Sewon Min, Ludwig Schmidt, Noah A. Smith, Mike Lewis*  [[abs](https://arxiv.org/abs/2210.03350)]

- **Least-to-most prompting enables complex reasoning in large language models** 2022.05 <br />
  *Denny Zhou, Nathanael Schärli, Le Hou, Jason Wei, Nathan Scales, Xuezhi Wang, Dale Schuurmans, Claire Cui, Olivier Bousquet, Quoc Le, Ed Chi*  [[abs](https://arxiv.org/abs/2205.10625)]

- **Learning to decompose: Hypothetical question decomposition based on comparable texts** 2022.10 <br />
*Ben Zhou, Kyle Richardson, Xiaodong Yu, Dan Roth* [[abs](https://arxiv.org/abs/2210.16865)]

- **Complexity-Based Prompting for Multi-Step Reasoning** 2022.05 <br />
*Yao Fu, Hao Peng, Ashish Sabharwal, Peter Clark, Tushar Khot* [[abs](https://arxiv.org/abs/2210.00720)]


### 💪 Reasoning Enhancement for Small LM
Objective: Enhance the Reasoning capability of small-scale LM models (<10B) and improve their performance on tasks such as mathematical reasoning, symbolic reasoning, common-sense reasoning, and task planning to achieve a level comparable to that of large-scale models (>100B).

#### Distillation
- **Symbolic Chain-of-Thought Distillation: Small Models Can Also “Think” Step-by-Step** 2023.06 <br />
*Liunian Harold Li, Jack Hessel, Youngjae Yu, Xiang Ren, Kai-Wei Chang, Yejin Choi* [[abs](https://arxiv.org/abs/2306.14050)]

- **Large Language Models Are Reasoning Teachers** 2023.06 <br />
*Namgyu Ho, Laura Schmid, Se-Young Yun* [[abs](https://arxiv.org/abs/2212.10071)]

- **Distilling Step-by-Step! Outperforming Larger Language Models with Less Training Data and Smaller Model Sizes** 2023.05 <br />
*Cheng-Yu Hsieh, Chun-Liang Li, Chih-Kuan Yeh, Hootan Nakhost, Yasuhisa Fujii, Alexander Ratner, Ranjay Krishna, Chen-Yu Lee, Tomas Pfister* [[abs](https://arxiv.org/abs/2305.02301)]

- **Distilling reasoning capabilities into smaller language models** 2023.07 <br />
*Shridhar K, Stolfo A, Sachan M. Distilling * [[abs](https://aclanthology.org/2023.findings-acl.441.pdf)]

- **Teaching Small Language Models to Reason** 2023.11 <br />
*Lucie Charlotte Magister, Jonathan Mallinson, Jakub Adamek, Eric Malmi, Aliaksei Severyn* [[abs](https://arxiv.org/abs/2212.08410)]

- **Explanations from Large Language Models Make Small Reasoners Better** 2022.10 <br />
*Shiyang Li, Jianshu Chen, Yelong Shen, Zhiyu Chen, Xinlu Zhang, Zekun Li, Hong Wang, Jing Qian, Baolin Peng, Yi Mao, Wenhu Chen, Xifeng Yan* [[abs](https://arxiv.org/abs/2210.06726)]

- **PINTO: Faithful Language Reasoning Using Prompt-Generated Rationales** 2022.11 <br />
*Peifeng Wang, Aaron Chan, Filip Ilievski, Muhao Chen, Xiang Ren* [[abs](https://arxiv.org/abs/2211.01562)]

#### Step-aware Reasoning
- **Enhancing Zero-Shot Chain-of-Thought Reasoning in Large Language Models through Logic** 2024.02 <br />
*Xufeng Zhao, Mengdi Li, Wenhao Lu, Cornelius Weber, Jae Hee Lee, Kun Chu, Stefan Wermter* [[abs](https://arxiv.org/abs/2309.13339)] [[code](https://github.com/xf-zhao/LoT)]

- **Training Verifiers to Solve Math Word Problems** 2021.10 <br />
*Karl Cobbe, Vineet Kosaraju, Mohammad Bavarian, Mark Chen, Heewoo Jun, Lukasz Kaiser, Matthias Plappert, Jerry Tworek, Jacob Hilton, Reiichiro Nakano, Christopher Hesse, John Schulman* [[abs](https://arxiv.org/abs/2110.14168)]

- **Solving Math Word Problems via Cooperative Reasoning induced Language Models** 2022.10 <br />
*Xinyu Zhu, Junjie Wang, Lin Zhang, Yuxiang Zhang, Yongfeng Huang, Ruyi Gan, Jiaxing Zhang, Yujiu Yang* [[abs](https://arxiv.org/abs/2210.16257)]

- **Making Large Language Models Better Reasoners with Step-Aware Verifier** 2022.06 <br />
*Yifei Li, Zeqi Lin, Shizhuo Zhang, Qiang Fu, Bei Chen, Jian-Guang Lou, Weizhu Chen* [[abs](https://arxiv.org/abs/2206.02336)]


####  Self-Training

- **STaR: Bootstrapping Reasoning With Reasoning** 2022.03 <br />
*Eric Zelikman, Yuhuai Wu, Jesse Mu, Noah D. Goodman* [[abs](https://arxiv.org/abs/2203.14465)]


- **Large Language Models Can Self-improve** 2022.10 <br />
*Jiaxin Huang, Shixiang Shane Gu, Le Hou, Yuexin Wu, Xuezhi Wang, Hongkun Yu, Jiawei Han* [[abs](https://arxiv.org/abs/2210.11610)]


### 📑 Survey

- **Reasoning with Language Model Prompting: A Survey**, 2022.12 <br />
*Shuofei Qiao, Yixin Ou, Ningyu Zhang, Xiang Chen, Yunzhi Yao, Shumin Deng, Chuanqi Tan, Fei Huang, Huajun Chen* [[abs](https://arxiv.org/abs/2212.09597)]

- **Towards Reasoning in Large Language Models: A Survey**, 2022.12 <br />
*Jie Huang, Kevin Chen-Chuan Chang* [[abs](https://arxiv.org/abs/2212.10403)]

- **A Survey of Deep Learning for Mathematical Reasoningy**, 2022.12 <br />
*Pan Lu, Liang Qiu, Wenhao Yu, Sean Welleck, Kai-Wei Chang* [[abs](https://arxiv.org/abs/2212.10535)]

- **Natural Language Reasoning, A Survey**, 2023.03 <br />
*Fei Yu, Hongbo Zhang, Prayag Tiwari, Benyou Wang* [[abs](https://arxiv.org/abs/2303.14725)]

<!---
## 🎉 Contributors
<a href="https://github.com/luban-agi/Awesome-Tool-Learning/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=luban-agi/Awesome-Tool-Learning"/>

</a>
-->
