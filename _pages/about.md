---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

[//]: # ()
[//]: # ()


**Hi 👋, I'm Mingxin.**

I am currently a first-year PhD student based in **Beijing**, currently affiliated with **Peking University**. I'm fortunate to be supervised by [Dr. Xinggong Zhang](https://www.wict.pku.edu.cn/NetVideo/).I received my bachelor's degree from **Huazhong University of Science and Technology (HUST)** that built a solid foundation in computer science and research, and have previously conducted research collaborations with researchers from the **Institute of Computing Technology, Chinese Academy of Sciences (ICT, CAS)** and **Harbin Institute of Technology (Shenzhen)**.


# 💡 Interests
- **AI Security**
  - Security, privacy, and alignment issues of large language models
  - Jailbreak, robustness, and misuse analysis

- **Network Security**
  - Malicious traffic detection
  - Encrypted traffic classification and website fingerprinting

- **AI Agents**
  More recently, I have been exploring **AI agents**, focusing on autonomous and tool-augmented LLM-based systems. I am interested in how agentic workflows and multi-agent collaboration can enable LLMs to solve complex, real-world tasks in a secure and controllable manner.

> I am always happy to connect with people who share interests in AI, security, and related research topics. I believe this is a field driven by diverse ideas and perspectives, and I am eager to learn through discussions and collaborations. Feel free to reach out.



<!-- ### Proficiencies
      
  **GPA:4.28/5.00** (or 3.70/4.00 according to [WES](https://www.wes.org/))

  |Course|Result|
  |:---:|:---:|
  |Calculus|97|
  |Software Engineering|97|
  |Algorithmic Design & Analysis|97|
  |Advanced Programming Language|94|
  |Computer Vision|94|
  |Principles of Imperative Computation|94|
  |Operating System|91|
  |Machine Learning|91|
  |...|...|
-->

<!-- # ⚙️ Skills
- Deep learning frameworks like Transformers, PyTorch, etc.
- Mechanistic Interpretability toolkits: NNsight, TransformerLens, SAELens. -->

# 📝 Selected Publications 

Please refer to my [Google Scholar](https://scholar.google.com/citations?user=iaBA__IAAAAJ) for full list of publications.

## 🧑‍🔬 AI for Security

**Vuldetectbench: Evaluating the deep capability of vulnerability detection with large language models**  <img src="https://img.shields.io/badge/Preprint-gray" alt="Preprint">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/PipeLineFinal_00.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Yu Liu\*, Lang Gao\*, **Mingxin Yang\***, Yu Xie, Ping Chen, Xiaojin Zhang, Wei Chen
(\*: Joint first authors)

*"A new benchmark, VulDetectBench, evaluates LLMs on program vulnerability detection and shows strong performance on coarse-grained tasks but poor capability in fine-grained vulnerability analysis."* 

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://arxiv.org/abs/2406.07595">Paper</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/Sweetaroo/VulDetectBench">Code</a></td>
</tr>
</table>

</div>
</div>

## AI Safety

**Unveiling the vulnerability of private fine-tuning in split-based frameworks for large language models: A bidirectionally enhanced attack**  <img src="https://img.shields.io/badge/CCS-2024-gray?labelColor=blue" alt="CCS 2024">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/bisr.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Guanzhong Chen, Zhenghan Qin, **Mingxin Yang**, Yajie Zhou, Tao Fan, Tianyu Du, Zenglin Xu

*"Expose privacy vulnerabilities in split learning for LLM fine-tuning and introduce BiSR, a powerful data reconstruction attack that can recover private training data even under existing defenses."* 

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://dl.acm.org/doi/abs/10.1145/3658644.3690295">Paper</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/StupidTrees/SplitLLM">Code</a></td>
</tr>
</table>

</div>
</div>

## 🧑‍🔬 Network Security

**Graph-Based Encrypted Malicious Traffic Detection Under Flow Distribution Drift With Flow Sampling**  <img src="https://img.shields.io/badge/APNet-2025-gray?labelColor=blue" alt="APNet 2025">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/gbt.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Yunpeng Tan, Qingyang Li, **Mingxin Yang**, Xinggong Zhang

*"Propose a flow-sampling-based graph construction method to mitigate flow distribution drift in encrypted traffic detection, significantly improving GNN accuracy and efficiency."*

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://dl.acm.org/doi/full/10.1145/3735358.3737756">Paper</a></td>
<!-- <td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/jugechengzi/Rationalization-A2I">Code</a></td> -->
</tr>
</table>

</div>
</div>

<!-- **Evaluate Bias without Manual Test Sets: A Concept Representation Perspective for LLMs**  <img src="https://img.shields.io/badge/Preprint-gray" alt="Preprint">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/PipeLineFinal_00.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Yu Liu, Lang Gao, **Mingxin Yang**, Yu Xie, Ping Chen, Xiaojin Zhang, Wei Chen

*"A new benchmark, VulDetectBench, evaluates LLMs on program vulnerability detection and shows strong performance on coarse-grained tasks but poor capability in fine-grained vulnerability analysis."* 

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://arxiv.org/abs/2406.07595">Paper</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/Sweetaroo/VulDetectBench">Code</a></td>
</tr>
</table>

</div>
</div> -->


<!-- **Shaping the Safety Boundaries: Understanding and Defending Against Jailbreaks in Large Language Models**  <img src="https://img.shields.io/badge/ACL-2025-gray?labelColor=blue" alt="ACL 2025">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/abd-pre.svg' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Lang Gao**, Jiahui Geng, Xiangliang Zhang, Preslav Nakov, and Xiuying Chen

*"Try to interpret common mechanisms of diverse LLM jailbreak attacks in the activation space and propose an efficient defense method."* 

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://aclanthology.org/2025.acl-long.1233/">Paper</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://mbzuai.ac.ae/news/how-jailbreak-attacks-work-and-a-new-way-to-stop-them/">MBZUAI News</a></td>
</tr>
</table>

</div>
</div> -->

<!-- **A Fano-Style Accuracy Upper Bound for LLM Single-Pass Reasoning in Multi-Hop QA**  <img src="https://img.shields.io/badge/Preprint-gray" alt="Preprint">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/fano.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Kaiyang Wan, **Lang Gao**, Honglin Mu, Preslav Nakov, Yuxia Wang, Xiuying Chen

*"LLM's accuracy will have a severe performance breakdown once the required information exceeds its internal capacity in complex multi-hop reasoning scenarios."* 

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://arxiv.org/pdf/2509.21199">Paper</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/KaiyangWan/InfoQA">Code</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://www.mittrchina.com/news/detail/15356">MIT Tech Review CN</a></td>
</tr>
</table>

</div>
</div> -->

<!-- **Adversarial Cooperative Rationalization: The Risk of Spurious Correlations in Even Clean Datasets**  <img src="https://img.shields.io/badge/ICML-2025-gray?labelColor=blue" alt="ICML 2025">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/a2i.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Wei Liu, Zhongyu Niu, **Lang Gao**, Zhiying Deng, Jun Wang, Haozhao Wang, and Ruixuan Li

*"An interpretable, causal learning paradigm that simultaneously avoids spurious correlations in data and traditional self-interpretable models."*

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://icml.cc/virtual/2025/poster/44947">Paper</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/jugechengzi/Rationalization-A2I">Code</a></td>
</tr>
</table>

</div>
</div> -->

## 👨‍🔧 Applications

**Linger: Intelligent Resume Parsing System**  <img src="https://img.shields.io/badge/Applications-2023-gray?labelColor=blue" alt="Applications 2023">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/resume.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Yifei Li, **Mingxin Yang**, Min Yang, Siyu Jiang

*"Under the guidance of Professor He Kun, our team proposed an Intelligent Resume Analysis System that leverages natural language processing and machine learning—integrating resume text recognition, large language models, and job–candidate matching algorithms—to efficiently and accurately parse resumes and address real-world recruitment challenges."*

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<!-- <td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://iclr.cc/virtual/2025/poster/30141">Paper</a></td> -->
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://www.cs.hust.edu.cn/info/1180/3284.htm">News</a></td>
<!-- <td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/UCSC-VLAA/MedTrinity-25M">Code <img src="https://img.shields.io/github/stars/UCSC-VLAA/MedTrinity-25M" alt="stars"></a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://huggingface.co/datasets/UCSC-VLAA/MedTrinity-25M">Dataset</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://yunfeixie233.github.io/MedTrinity-25M/">Website</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://docs.google.com/forms/d/e/1FAIpQLSfjNvzyo2LRpAvLfGpj6XmNI_OHaVDRtV0ON2pcz1dUYC5Itg/viewform">Expert Eval</a></td> -->
</tr>
</table>

</div>
</div>



<!-- **DyFlow: Dynamic Workflow Framework for Agentic Reasoning**  <img src="https://img.shields.io/badge/NeurIPS-2025-gray?labelColor=blue" alt="NeurIPS 2025">

<div class='paper-box'><div class='paper-box-image'><div><img src='files/dyflow.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

Yanbo Wang, Zixiang Xu, Yue Huang, Xiangqi Wang, Zirui Song, **Lang Gao**, Chenxi Wang, Xiangru Tang, Yue Zhao, Arman Cohan, Xiangliang Zhang, and Xiuying Chen

*"DyFlow is a dynamic workflow framework for LLM-based agents, that adapts its reasoning steps in real-time using intermediate feedback, enabling better generalisation across diverse tasks."*

<table style="border: 1px solid #ddd; border-collapse: collapse; margin-top: 10px;">
<tr>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://arxiv.org/abs/2509.26062">Paper</a></td>
<td style="border: 1px solid #ddd; padding: 5px 10px;"><a href="https://github.com/wyf23187/DyFlow">Code</a></td>
</tr>
</table>

</div>
</div> -->




<!-- 
[//]: # (# ⚙️ Project)

[//]: # ()
[//]: # (**TrustLLM: Trustworthiness in Large Language Models**)

[//]: # ()
[//]: # ()
[//]: # ()
[//]: # ()
[//]: # ()
[//]: # ()
[//]: # ()
[//]: # (- We have proposed a set of guidelines based on a comprehensive literature review for evaluating the trustworthiness of LLMs, which is a taxonomy encompassing eight aspects, including *truthfulness, safety, fairness, robustness, privacy, machine ethics, transparency, and accountability*.)

[//]: # (- We have established a benchmark for six of these aspects due to the difficulty of benchmarking transparency and accountability. This is the first comprehensive and integrated benchmark comprising over 18 subcategories, covering more than 30 datasets and 16 LLMs, including proprietary and open-weight ones.)

[//]: # (- We obtain empirical findings from the results of our experiments, which provide valuable insights for future research.)

[//]: # (📣 **Welcome your Contribution**)

[//]: # ()
[//]: # (We welcome your contributions, including but not limited to the following:)

[//]: # ()
[//]: # (- New benchmark datasets of trustworthy dimension)

[//]: # (- Research on trustworthy issues of LLM)

[//]: # (- Improvements to the [trustllm toolkit]&#40;https://github.com/HowieHwong/TrustLLM&#41;) -->

# 🧐 Service
<!-- - 2024, Reviewer: ACL, EMNLP, NLPCC. -->
- 2025, Open Source Summer Campus Ambassador

# 💼 Experiences
- \[10 / 2022 - 07 / 2024      \] <img src='files/hust.png' style='width: 1.2em;'> HUST (Supervisor: [Prof. Kun He](http://faculty.hust.edu.cn/hekun/zh_CN/index.htm), topic: Jailbreak)
- \[07 / 2023 - 01 / 2024\] <img src='files/hust.png' style='width: 1.2em;'> HUST (Supervisor: [Prof. Wei Chen](http://faculty.hust.edu.cn/CHENWEI/zh_CN/), topic: Code Detection)
- \[12 / 2023 - 12 / 2024\] <img src='files/hit.jpg' style='width: 1.2em;'> Harbin Institute of Technology, Shenzhen (Supervisor: [Guanzhong Chen](https://stupidtrees.github.io), topic: Split-Learning in Large Language Model)
- \[03 / 2024 - 06 / 2024\] <img src='files/CAS.png' style='width: 1.2em;'> Institute of Computing Technology, Chinese Academy of Sciences (Supervisor: [Prof. Fei Sun](https://scholar.google.com/citations?hl=zh-CN&user=OlRxBhcAAAAJ&view_op=list_works&sortby=pubdate), topic: AI Safety)
> 💬 I am deeply grateful to all the mentors and collaborators who have guided and supported me along the way. Your encouragement, trust, and inspiration have made all the difference in my journey.

# 📖 Educations
  *08 / 2025 - Now* : Ph.D. student, <img src='files/pku.png' style='width: 1.2em;'> Peking University

  *09 / 2021 - 07 / 2025* : B.E., <img src='files/hust.png' style='width: 1.2em;'> Huazhong University of Science and Technology

<!-- # 🏆 Honors and Awards
- 🥇 **National First Price**, RAICOM Robotics Developer Contest - CAIR Engineering Competition National Finals，2024
- 🥈 **National Second Price**, 15th China College Students' Service Outsourcing Innovation and Entrepreneurship Competition, 2024
- 🥈 **National Second Prize**, The 5th Integrated Circuit EDA Design Elite Challenge (Deep Learning Track), 2023
- 🥉 **National Third Prize**, The 5th Global Campus Artificial Intelligence Algorithm Elite Competition, 2023. 
- 🥉 **National Third Prize**, iFlytek Developer Competition, NLP Track, 2023
-->


# 🧩Miscellaneous
<!-- ## 📚 Resources
### Insights
- Book: Interpretability in Deep Learning \[[Link](files/XAI.pdf)\]
- Book: Interpretable Machine Learning \[[Link](https://christophm.github.io/interpretable-ml-book/index.html)\]
- Book: Trustworthy Machine Learning \[[Link](https://arxiv.org/pdf/2310.08215)\]
- Book: 大语言模型 \(The Chinese Book for Large Language Models\) \[[Link](https://llmbook-zh.github.io/LLMBook.pdf)\]
- Article: The Bitter Lesson \[[Link](files/bitter_lesson.pdf)\]
- Article: The Urgency of Interpretability \[[Link](https://www.darioamodei.com/post/the-urgency-of-interpretability)\]


### Blogs

- \[05/24\] \[Chinese\] National Undergraduate Innovation Project Documentation. \[[Link](files/grammargpt-rp.pdf)\] 
- \[03/24\] \[Chinese\] Negative Transfer. \[[Link](https://k034sybliz3.feishu.cn/wiki/GX7Vw4IfBiYq6okUDf7cAGCJnHh)\] 
- \[03/24\] \[Chinese\] Mixture of Experts Explained. \[[Link](https://k034sybliz3.feishu.cn/wiki/MjBFwFm9giBTg3kQ9v6cJ7uQnFb)\] 
- \[01/24\] \[Chinese\] EMNLP2020 Tutorial Notes (Topic: Explainable AI). \[[Link](https://k034sybliz3.feishu.cn/wiki/Mo2xwR6B4iDV7nk4CZ5clwymnze)\] 

## Other Stuff
I also like photography. Sometimes I take good photos by accident. So I might upload a few here someday, along with some unnecessary commentary, but feel free to pretend you're looking forward to it.🙃 -->

---

<div style="text-align: center;">
<script type='text/javascript' id='mapmyvisitors' src='https://mapmyvisitors.com/map.js?cl=bdc1c4&w=600&t=n&d=RJ-9BpR3nPPhm7slE3OgXRPbI71Yo8jKNdXiKoeSQUw&co=f3eee8&ct=808080&cmo=3acc3a&cmn=ff5353'></script>
</div>


