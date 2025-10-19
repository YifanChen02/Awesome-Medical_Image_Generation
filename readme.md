# Awesome-Medical Image Generation


# News

# Introduction

# Contents
- [0 survey](#0-survey)
  - [0.1 image translation](#image-translation)
  - [0.2 image synthesis](#image-synthesis)
  - [0.3 image fusion](#image-fusion)
  - [0.4 image restoration](#image-restoration)

- [1. 🧠 Image Synthesis](#1-image-synthesis)
  - [1.1 GAN-based](#11-gan-based)
  - [1.2 Transformer-based](#12-transformer-based)
  - [1.3 Diffusion-based](#13-diffusion-based)
  - [1.4 Mamba-based](#14-mamba-based)
  - [1.5 Diffusion + Transformer](#15-diffusion--transformer)

- [2. 🔄 Image Translation](#2-image-translation)
  - [2.1 GAN-based](#21-gan-based)
  - [2.2 Diffusion-based](#22-diffusion-based)
  - [2.3 Mamba-Diffusion](#23-mamba-diffusion)
  - [2.4 Others (Image Translation)](#24-others-image-translation)

- [3. 🔗 Image Fusion](#3-image-fusion)

- [4. 🖼️ Image Generation](#4-image-generation)

- [5. 🧽 Image Restoration](#5-image-restoration)
  - [5.0 General Restoration](#50-general-restoration)
  - [5.1 Inpainting](#51-inpainting)
  - [5.2 Super Resolution](#52-super-resolution)
  - [5.3 Denoising](#53-denoising)
  - [5.4 Enhancement](#54-enhancement)

- [6 image reconstruction](#6-image-reconstruction)

- [7 image augmentation](#7-image-augmentation)

- [Taxonomy](#Taxonomy)
  - [Image Generation Taxonomy](#Image-Generation-Taxonomy)
  
- [Modalities](#Modalities)
  - [MR](MR)
  - [CT](CT)
    
- [📂 Dataset Process & Structure](#dataset-process--structure)
  - [MR](MR)
    - [Brain](#brats17)
    - [Breast](#breast)
  - [CT](#CT)
    - [Uterus Ovary](#uterus-ovary)
    - [Adrenal](#adrenal)
    - [Bladder Kidney](#bladder-kidney)
    - [Lung](#lung)
    - [Stomach Colon Liver Pancreas](#stomach-colon-liver-pancreas)




# Taxonomy
## Image Generation Taxonomy
![Alt text](https://github.com/YifanChen-thu/Medical_Multi-Modal_Generation/blob/main/Mechanism_Architecture_page-0001.jpg)
![Alt text](https://github.com/YifanChen-thu/Medical_Multi-Modal_Generation/blob/main/ImageGeneration_page-0001.jpg)

# Modalities
## MR
![Alt text](https://github.com/YifanChen-thu/Multi-modal_MRI_Synthesis_Paper_List/blob/main/MR_Relation_S.png)
```markdown
医学成像技术
└── 磁共振成像 (MRI)
    ├── 解剖成像 (Anatomical Imaging)
    │   ├── T1加权成像 (T1-weighted Imaging, T1)
    │   │   ├── 常规T1 (Conventional T1)
    │   │   └── T1C (T1 with Contrast) - 对比增强T1
    │   │       └── 通过注射对比剂 (e.g., Gadolinium) 提高病变区域对比度
    │   ├── T2加权成像 (T2-weighted Imaging, T2)
    │   └── 脂肪抑制技术 (Fat Suppression Techniques)
    │       ├── FLAIR (Fluid Attenuated Inversion Recovery) - 液体衰减反转恢复
    │       │   └── 抑制液体信号，提高病变（如多发性硬化）可见性
    │       └── PD (Proton Density) - 质子密度加权成像
    │           └── 对比强调不同组织的质子密度，主要用于关节和脑部成像
    ├── 弥散成像 (Diffusion Imaging)
    │   ├── 弥散加权成像 (DWI - Diffusion Weighted Imaging)
    │   │   ├── 反映水分子在三个方向上的扩散特性，敏感于急性缺血性脑损伤等
    │   │   └── 表观弥散系数 (ADC - Apparent Diffusion Coefficient)
    │   │       └── 从DWI图像计算得到，用于定量分析水分子扩散特性
    │   └── 扩散张量成像 (DTI - Diffusion Tensor Imaging)
    │       ├── 反映水分子在多个方向上的扩散特性，用于分析复杂的组织结构
    │       ├── 分数各向异性 (FA - Fractional Anisotropy)
    │       │   └── 表示水分子扩散的各向异性程度，数值范围从0到1，用于评估组织的方向性
    │       └── 平均扩散率 (MD - Mean Diffusivity)
    │           └── 表示水分子在所有方向上的平均扩散强度，用于综合评估组织的扩散特性
    ├── 功能成像 (Functional Imaging)
    │   ├── resting-state fMRI - 静息态功能磁共振成像
    │   └── task fMRI - 任务态功能磁共振成像
    ├── 灌注成像 (Perfusion Imaging)
    │   ├── DSC (Dynamic Susceptibility Contrast) - 动态敏感对比增强
    │   │   └── 通过注射对比剂测量血流量，常用于评估脑肿瘤和中风
    │   ├── DCE (Dynamic Contrast-Enhanced) - 动态对比增强成像
    │   │   └── 评估组织中对比剂的动态分布，常用于肿瘤血管生成的研究
    │   └── ASL (Arterial Spin Labeling) - 动脉自旋标记
    │       └── 不使用对比剂，通过标记动脉血水分子来测量血流量
    └── 双极磁化成像 (Bipolar Imaging, bp)
        └── 通过改变磁场梯度来增强图像对比度，不使用对比剂

  


```
## CT
![Alt text](https://github.com/YifanChen-thu/Medical_Multi-Modal_Generation/blob/main/CT分类.png)


# Paper & Code & Dataset
## 0 survey
### image translation
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|AI4Research: A Survey of Artificial Intelligence for Scientific Research.[[paper](https://arxiv.org/pdf/2507.01903)][[code](https://github.com/LightChen233/Awesome-AI4Research)]|arxiv202507||||
|2|Deep learning-based techniques for estimating high-quality full-dose positron emission tomography images from low-dose scans: a systematic review[[paper](https://link.springer.com/article/10.1186/s12880-024-01417-y)]|BMC Medical Imaging. 2024||||
|3|A review on cross-contrast MRI image synthesis through deep learning[[paper](https://link.springer.com/article/10.1007/s44352-025-00012-3)]|Discover Imaging. 2025||||
|4|Advancements in synthetic CT generation from MRI: A review of techniques, and trends in radiation therapy planning[[paper](https://aapm.onlinelibrary.wiley.com/doi/full/10.1002/acm2.14499)]|Journal of Applied Clinical Medical Physics. 2024||||
|5|A systematic literature review: deep learning techniques for synthetic medical image generation and their applications in radiotherapy[[paper](https://www.frontiersin.org/journals/radiology/articles/10.3389/fradi.2024.1385742/full)]|Frontiers in Radiology. 2024||||
|6|Cross-modality neuroimage synthesis: A survey[[paper](https://dl.acm.org/doi/abs/10.1145/3625227)][[code](https://github.com/M-3LAB/awesome-multimodal-brain-image-systhesis)]|ACM computing surveys. 2023||||
|7|Machine learning for medical image translation: A systematic review[[paper](https://www.mdpi.com/2306-5354/10/9/1078)]|Bioengineering. 2023 ||||
|8|Deep learning based synthesis of MRI, CT and PET: Review and analysis[[paper](https://www.sciencedirect.com/science/article/pii/S1361841523003067)]|Medical image analysis. 2024||||
|9|Medical image translation with deep learning: Advances, datasets and perspectives[[paper](https://www.sciencedirect.com/science/article/pii/S1361841525001525)]|Medical Image Analysis. 2025 ||||

### image synthesis
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Synthetic data generation methods in healthcare: A review on open-source tools and methods[[paper](https://www.sciencedirect.com/science/article/pii/S2001037024002393)]|Computational and structural biotechnology journal 2024||||
|2|A systematic review of generative AI approaches for medical image enhancement: Comparing GANs, transformers, and diffusion models[[paper](https://www.sciencedirect.com/science/article/pii/S1386505625001200)]|International journal of medical informatics 2025||||
|3|Survey: application and analysis of generative adversarial networks in medical images[[paper](https://link.springer.com/article/10.1007/s10462-024-10992-z)]|Artificial Intelligence Review 2024||||
|4|Synthetic data in radiological imaging: current state and future outlook[[paper](https://academic.oup.com/bjrai/article/1/1/ubae007/7679083)]|Artificial Intelligence 2024||||
|5|Diffusion Models for Medical Image Computing: A Survey[[paper](https://ieeexplore.ieee.org/abstract/document/10676408)]|Tsinghua Science and Technology 2025||||
|6|Diffusion models in medical imaging: A comprehensive survey[[paper](https://www.sciencedirect.com/science/article/pii/S1361841523001068)]|Medical image analysis. 2023||||
|7|Review of Medical Image Synthesis using GAN Techniques .[[paper](https://www.itm-conferences.org/articles/itmconf/pdf/2021/02/itmconf_icitsd2021_01005.pdf)]|ITM Web of Conferences,2021||||

### image restoration
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|.[[paper]()]||||
|2|.[[paper]()]||||
|3|.[[paper]()]||||
|4|.[[paper]()]||||
|5|.[[paper]()]||||

### image fusion
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|2|The generative era of medical AI.[[paper](https://www.cell.com/cell/fulltext/S0092-8674(25)00568-9)]|cell 2025||||
|3|Survey on Adversarial Attack and Defense for Medical Image Analysis: Methods and Challenges.[[paper](https://arxiv.org/pdf/2303.14133)]|ACM Computing Surveys 2025||||
|4|Addressing missing modality challenges in MRI images: A comprehensive review.[[paper](https://www.sciopen.com/article/save_anchor/1920366619911577601.pdf)]|Computational Visual Media 202504||||
|5|Unsupervised deep learning-based medical image registration: a survey.[[paper](https://iopscience.iop.org/article/10.1088/1361-6560/ad9e69/pdf)]|Physics in Medicine and Biology 2025||||
|6|Prompt Mechanisms in Medical Imaging: A Comprehensive Survey.[[paper](https://arxiv.org/pdf/2507.01055)]|arxiv，20250628||||
|7|Medical image translation with deep learning: Advances, datasets and perspectives.[[paper](https://doi.org/10.1016/j.media.2025.103605)]|Medical Image Analysis 202507||||
|8|Cross-Modality Neuroimage Synthesis: A Survey.[[paper](https://arxiv.org/pdf/2202.06997)][[code](https://github.com/M-3LAB/awesome-multimodal-brain-image-systhesis.)]|arxiv，20230921||||
|9|Deep learning in medical image super resolution: a review.[[paper](https://link.springer.com/article/10.1007/s10489-023-04566-9)]|Applied Intelligence 2023|||
|10|A survey on automatic generation of medical imaging reports based on deep learning.[[paper](https://link.springer.com/article/10.1186/s12938-023-01113-y)][[code]()]|Springer Nature Link 2023 05 18||||
|11|Applications of deep learning in medical imaging: a survey.[[paper](https://www.researchgate.net/publication/345341771_Applications_of_deep_learning_in_medical_imaging_a_survey)]|||||
|12|Continual Learning in Medical Imaging: A Survey and Practical Analysis.[[paper](https://arxiv.org/pdf/2405.13482)]|arxiv,2024||||
|13|Survey On Medical Image Classification Using CAPSGNN.[[paper](https://www.researchgate.net/publication/371910798_Survey_On_Medical_Image_Classification_Using_CAPSGNN)]|Recent Research Reviews Journal 2023|||
|14|Deep Learning in Medical Image Super-Resolution: A Survey.[[paper](https://ijettjournal.org/Volume-71/Issue-8/IJETT-V71I8P201.pdf)]|International Journal of Engineering Trends and 2023|||
|15|Overview of image‑to‑image translation by use of deep neural networks: denoising, super‑resolution, modality conversion, and reconstruction in medical imaging.[[paper](https://link.springer.com/article/10.1007/s12194-019-00520-y)]|adiological Physics and Technology 2019||||
|16|.[[paper]()]||||
|17|.[[paper]()]||||


———————以下为待整理的———————————


|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Survey: application and analysis of generative adversarial networks in medical images.[[paper](https://link.springer.com/article/10.1007/s10462-024-10992-z)]|Artificial Intelligence Review 2025||||
|2|Generative adversarial networks in medical image reconstruction: A systematic literature review.[[paper](https://www.sciencedirect.com/science/article/pii/S0010482525004457)]|Computers in Biology and Medicine 2025|||
|3|Data-GAN Augmentation Techniques in Medical Image Analysis: A Deep Survey.[[paper](https://link.springer.com/article/10.1007/s42979-025-03867-9)]|SN Computer Science 2025|||
|4|Generative Adversarial Networks in Medical Image Analysis: A Comprehensive Survey.[[paper](https://link.springer.com/content/pdf/10.1007/978-981-97-4149-6_26.pdf)]|International Conference On Innovative Computing And Communication 2024|||
|5|A Review of Generative Adversarial Networks (GANs) and Its Applications in a Wide Variety of Disciplines: From Medical to Remote Sensing.[[paper]([https://ieeexplore.ieee.org/document/10372211](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10372211))]|IEEE Access 2023|||
|6|Generative Adversarial Networks in Medical Image augmentation: A review.[[paper](https://www.sciencedirect.com/science/article/pii/S0010482522001743)]|Computers in Biology and Medicine 2022||||
|7| Application of generative adversarial networks (GAN) for ophthalmology image domains: a survey.[[paper](https://link.springer.com/content/pdf/10.1186/s40662-022-00277-3.pdf?pdf=core)]|Eye and Vision 2022|||
|8|Application of generative adversarial networks (GAN) for ophthalmology image domains: a survey.[[paper](https://eandv.biomedcentral.com/articles/10.1186/s40662-022-00277-3)]Eye and Vision 2022||||
|9|Synthesis of diagnostic quality cancer pathology images by generative adversarial networks.[[paper](https://pathsocjournals.onlinelibrary.wiley.com/doi/epdf/10.1002/path.5509?saml_referrer)]|The Journal of Pathology 2020|||




transformer-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Advances in medical image analysis with vision Transformers: A comprehensive review.[[paper](https://www.sciencedirect.com/science/article/pii/S1361841523002608?via%3Dihub)][[code](https://github.com/xmindflow/Awesome-Transformer-in-Medical-Imaging)]|Medical Image Analysis 2024||||
|2|Transformers in medical imaging: A survey.[[paper](https://www.sciencedirect.com/science/article/pii/S1361841523000634?via%3Dihub)][[code](https://github.com/fahadshamshad/awesome-transformers-in-medical-imaging)]|Medical Image Analysis 2023||||
|3|A survey of Transformer applications for histopathological image analysis: New developments and future directions.[[paper](https://biomedical-engineering-online.biomedcentral.com/articles/10.1186/s12938-023-01157-0)][[code](https://github.com/S-domain/Survey-Paper)]|BioMedical Engineering OnLine 2023||||
|4|Predictive Analytics and Machine Learning for Medical Informatics A Survey of Tasks and Techniques.[[paper](https://www.researchgate.net/publication/349290707_Predictive_Analytics_and_Machine_Learning_for_Medical_Informatics_A_Survey_of_Tasks_and_Techniques#read)]|Machine Learning, Big Data, and IoT for Medical Informatics 2021||||

diffusion-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Foundation Models for Music: A Survey.[[paper](https://arxiv.org/abs/2408.14340)][[code](https://github.com/nicolaus625/FM4Music)]|arXiv, 2024||||
|2|A Comprehensive Survey on Diffusion Models and Their Applications.[[paper](https://arxiv.org/abs/2408.10207)][[code]()]|arXiv, 2024||||
|3|Physics-Inspired Generative Models in Medical Imaging: A Review.[[paper](https://arxiv.org/abs/2407.10856)]|arXiv, 2024||||
|4|Diffusion Models in Low-Level Vision: A Survey.[[paper](https://arxiv.org/abs/2406.11138)][[code](https://github.com/ChunmingHe/awesome-diffusion-models-in-low-level-vision)]|arXiv, 2024||||
|5|Artifact Reduction in 3D and 4D Cone-beam Computed Tomography Images with Deep Learning -- A Review.[[paper](https://arxiv.org/abs/2403.18565)][[code]()]|arXiv, 2024||||
|6|A Survey of Emerging Applications of Diffusion Probabilistic Models in MRI.[[paper](https://arxiv.org/abs/2311.11383)][[code]()]|arXiv, 2023||||
|7|A Comprehensive Review of Generative AI in Healthcare.[[paper](https://arxiv.org/abs/2310.00795)][[code]()]|arXiv, 2023||||
|8|A Survey on Graph Diffusion Models: Generative AI in Science for Molecule, Protein and Material.[[paper](https://arxiv.org/abs/2304.01565)][[code]()]|arXiv, 2023||||
|9|Diffusion Models for Time Series Applications: A Survey.[[paper](https://arxiv.org/abs/2305.00624)][[code]()]|arXiv, 2023||||
|10|A Comprehensive Survey on Knowledge Distillation of Diffusion Models.[[paper](https://arxiv.org/abs/2304.04262)][[code]()]|arXiv, 2023||||
|11|Generative AI for Medical Imaging: extending the MONAI Framework.[[paper](https://arxiv.org/abs/2307.15208)][[code](https://github.com/Project-MONAI/GenerativeModels)]|arXiv, 2023||||
|12|Deep Learning Approaches for Data Augmentation in Medical Imaging: A Review.[[paper](https://arxiv.org/abs/2307.13125)][[code]()]|Journal of Imaging, 2023||||
|13|A Comprehensive Survey on Generative Diffusion Models for Structured Data.[[paper](https://arxiv.org/abs/2306.04139)][[code]()]|arXiv, 2023||||
|14|Diffusion Models in Medical Imaging: A Comprehensive Survey.[[paper](https://arxiv.org/abs/2211.07804)][[code]()]|MedIA Journal, 2023||||
|15|Efficient Diffusion Models for Vision: A Survey.[[paper](https://arxiv.org/abs/2210.09292)][[code]()]|arXiv, 2022||||
|16|Diffusion Models in Vision: A Survey.[[paper](https://arxiv.org/pdf/2209.04747.pdf)][[code](https://github.com/CroitoruAlin/Diffusion-Models-in-Vision-A-Survey)]|arXiv, 2022||||
|17|A Survey on Generative Diffusion Model.[[paper](https://arxiv.org/pdf/2209.02646.pdf)][[code](https://github.com/chq1155/A-Survey-on-Generative-Diffusion-Model)]|arXiv, 2022||||
|18|Diffusion Models: A Comprehensive Survey of Methods and Applications.[[paper](https://arxiv.org/pdf/2209.00796)][[code](https://github.com/YangLing0818/Diffusion-Models-Papers-Survey-Taxonomy)]|arXiv, 2022||||


mamba-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|A Comprehensive Survey of Mamba Architectures for Medical Image Analysis: Classification, Segmentation, Restoration and Beyond.[[paper](https://arxiv.org/pdf/2410.02362)][[code](https://github.com/Madhavaprasath23/Awesome-Mamba-Papers-On-Medical-Domain)]|arxiv20241003||||
|2|A comprehensive survey for Hyperspectral Image Classification: The evolution from conventional to transformers and Mamba models.[[paper](https://arxiv.org/pdf/2410.02362)]|Neurocomputing 2025||||

———————以上为待整理的———————————


## 1 Image synthesis
### 1.1 GAN-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Synthetic PET from CT improves diagnosis and prognosis for lung cancer: Proof of concept.[[paper](https://www.sciencedirect.com/science/article/pii/S2666379124001071?via%3Dihub)]|Cell Reports Medicine 24|||Lung|
|2|Image Synthesis in Multi-Contrast MRI With Conditional Generative Adversarial Networks.[[paper](https://ieeexplore.ieee.org/abstract/document/8653423)][[code](https://github.com/icon-lab/pGAN-cGAN)]|TMI 19|||Brain|
|3|Memory-Efficient 3D High-Resolution Medical Image Synthesis Using CRF-Guided GANs.[[paper](https://arxiv.org/pdf/2503.10899)]|arXiv,20250313|||Lung,Brain|
|4|HealthiVert-GAN: A Novel Framework of Pseudo-Healthy Vertebral Image Synthesis for Interpretable Compression Fracture Grading.[[paper](https://arxiv.org/pdf/2503.05990)][[code](https://huggingface.co/ZhangqiSJTU/HealthiVert-GAN)]|arXiv,20250508|||bone|
|5|A Self-attention Guided Multi-scale Gradient GAN for Diversi ed X-ray Image Synthesis.[[paper](https://arxiv.org/pdf/2210.06334)]|arXiv,20221112||X-ray||
|6|Pathology Synthesis of 3D-Consistent Cardiac MR Images using 2D VAEs and GANs.[[paper](https://arxiv.org/pdf/2209.04223)][[code](https://github.com/sinaamirrajab/CardiacPathologySynthesis)]|machine learning for biomedical imaging,20230530|||heart|
|7|Backdoor Attack is A Devil in Federated GAN-based Medical Image Synthesis.[[paper](https://arxiv.org/pdf/2207.00762)][[code](https://github.com/Nanboy-Ronan/Backdoor-FedGAN)]|arXiv,20220730||||
|8|Bi-Modality Medical Image Synthesis Using Semi-Supervised Sequential Generative Adversarial Networks.[[paper](https://arxiv.org/pdf/2308.14066)][[code](https://github.com/hustlinyi/Multimodal-Medical-Image-Synthesis.)]|arXiv,20230829||||
|9|Realistic Chest X-Ray Image Synthesis via Generative Network with Stochastic Memristor Array for Machine Learning-Based Medical Diagnosis.[[paper](https://advanced.onlinelibrary.wiley.com/doi/epdf/10.1002/adfm.202305136)]|Advanced Functional Materials，20240401||X-ray||
|10|An innovative medical image synthesis based on dual GAN deep neural networks for improved segmentation quality.[[paper](https://link.springer.com/content/pdf/10.1007/s10489-022-03682-2.pdf)]|Springer Nature,2022||||
|11|HLSNC-GAN: Medical Image Synthesis Using Hinge Loss and Switchable Normalization in CycleGAN.[[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10504113)]|IEEE Access,20240322||||
|12|ADGAN: Adaptive Domain Medical Image Synthesis Based on Generative Adversarial Networks.[[paper](https://www.sciopen.com/article/save_anchor/1800781372023480322.pdf)]|CAAI Artificial Intelligence Research,20241201|||brain|
|13|ADGAN: Attribute-Driven Generative Adversarial Network for Synthesis and Multiclass Classification of Pulmonary Nodules.[[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9833464)]|IEEE Transactions on Neural Networks and Learning Systems,202402|||lung|
|14|medigan: a Python library of pretrained generative models for medical image synthesis.[[paper](https://arxiv.org/pdf/2209.14472)][[code](https://github.com/richardobi/medigan?tab=readme-ov-file)]|Journal of Medical Imaging,20230223||||
|15|Medical Image Synthesis with Generative Adversarial Networks for Tissue Recognition.[[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8419363)]|||||



|17|Conditional Variational Autoencoder with Balanced Pre-training for Generative Adversarial Networks.[[paper](https://doi.org/10.1109/DSAA54385.2022.10032367)][[code](https://github.com/alibraytee/CAPGAN )]|IEEE 9th International Conference on Data Science and Advanced Analytics (DSAA),2022||||
|18|Correction of Out-of-Focus Microscopic Images by Deep Learning .[[paper](https://doi.org/10.1016/j.csbj.2022.04.003)][[code](https://github.com/jiangdat/COMI)]|Comput Struct Biotechnol J 2022||||
|19|DDcGAN: A Dual-Discriminator Conditional Generative Adversarial Network for Multi-Resolution Image Fusion .[[paper](https://doi.org/10.1109/TIP.2020.2977573)][[code](https://github.com/jiayi-ma/DDcGAN)]|  IEEE Trans Image Process 2020||||
|20|DC-cycleGAN: Bidirectional CT-to-MR synthesis from unpaired data.[[paper](https://doi.org/10.1016/j.compmedimag.2023.102249)][[code](https://github.com/JiayuanWang-JW/DC-cycleGAN )]| Comput Med Imaging Graph 2023||||
|21|Staingan: Stain Style Transfer for Digital Histological Images .[[paper](https://doi.org/10.1109/ISBI.2019.8759152)][[code](https://github.com/xtarx/StainGAN )]|ISBI 2019||||
|22|MRI-Based Radiomics Combined with Deep Learning for Distinguishing IDH-Mutant WHO Grade 4 Astrocytomas from IDH-Wild-Type Glioblastomas.[[paper](https://doi.org/10.3390/cancers15030951)][[code](https://github.com/kasaai/ctgan?tab=readme-ov-file)]|Cancers 2023||||
|23|Overcoming data scarcity in radiomics/radiogenomics using synthetic radiomic features.[[paper](https://doi.org/10.1016/j.compbiomed.2024.108389)][[code](https://github.com/sdv-dev/SDV )]|Comput Biol Med 2024||||
|24|TS-GAN: Time-series GAN for Sensor-based Health Data Augmentation.[[paper](https://doi.org/10.1145/3583593)]|ACM Trans Comput Healthc 2023||||
|25|Generalized Generative Deep Learning Models for Biosignal Synthesis and Modality Transfer.[[paper]( https://doi.org/10.1109/JBHI.2022.3223777)][[code](https://github.com/theekshanadis/biosignalGANs)]|IEEE J Biomed Health Inform 2023||||
|26|.[[paper]()][[code]()]|  ||||
|27|.[[paper]()][[code]()]|  ||||
|28|.[[paper]()][[code]()]|  ||||

### 1.2 Transformer-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|ResViT: Residual vision transformers for multi-modal medical image synthesis.[[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9758823)][[code1](https://github.com/icon-lab/ResViT) [code2](https://github.com/CV-Reimplementation/ResViT-Reimplementation)]|TMI22|[[BrainMRI:IXI] [BraTS] [PelvisCT-MRI]|MRI(T1,T2,PD,FLAIR) & MRI->CT| Brain |
|2|One Model to Synthesize Them All: Multi-Contrast Multi-Scale Transformer for Missing Data Imputation.[[paper](https://arxiv.org/pdf/2204.13738)]|TMI23|||Brain|
|3|VTGAN:Semi-supervised Retinal Image Synthesis and Disease Prediction using Vision Transformers.[[paper](https://arxiv.org/pdf/2104.06757)]|arXiv,20210813|||Retina|
|4|Cross-Model Transformer Method for Medical Image Synthesis.[[paper](https://onlinelibrary.wiley.com/doi/epdf/10.1155/2021/5624909)]|Data-Enabled Intelligence in Complex Industrial Systems,20211025||||
|5|TTS-GAN: A Transformer-based Time-Series Generative Adversarial Network.[[paper](http://arxiv.org/abs/2202.02691)][[code]( https://github.com/imics-lab/tts-gan)]|arxiv，2022||||
|6|.[[paper]()][[code]()]|||||
|7|.[[paper]()][[code]()]|||||
|8|.[[paper]()][[code]()]|||||


### 1.3 Diffusion-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1| MedM2G: Unifying Medical Multi-Modal Generation via Cross-Guided Diffusion with Visual Invariant.[[paper](https://arxiv.org/abs/2403.04290)]| CVPR24 |[X-ray:[MIMIC-CXR](https://arxiv.org/abs/1901.07042)] [contextual medical images:[MedICat](https://github.com/allenai/medicat)] [[kaggle:MRI-CT](https://www.kaggle.com/datasets/chenghanpu/brain-tumor-mri-and-ct-scan)]|MRI<->MRI<->CT<->X-ray & text<->image<->image|Brain|
|2|CoLa-Diff: Conditional Latent Diffusion Model for Multi-Modal MRI Synthesis.[[paper](https://arxiv.org/abs/2303.14081)] | MICCAI23 |[[BraTS18]()] [[IXI]()]| MRI(T1,T1ce,T2,FLAIR) & MRI(T1,T2,PD) |Brain|
|3|Phy-Diff: Physics-guided Hourglass Diffusion Model for Diffusion MRI Synthesis.[[paper](https://arxiv.org/abs/2406.03002)]|MICCAI24|||Brain|
|4|Conditional Diffusion Models for Semantic 3D Brain MRI Synthesis.[[paper](https://arxiv.org/pdf/2305.18453)]|||||
|5|Temporal evolution of knee osteoarthritis: A diffusion-based morphing model for x-ray medical image synthesis.[[paper](https://arxiv.org/pdf/2408.00891)]|arXiv, 20240801|||knee|
|6|Brain PET Synthesis from MRI Using Joint Probability Distribution of Diffusion Model at Ultrahigh Fields.[[paper](https://arxiv.org/abs/2211.08901)]|arXiv, 2022||||
|7|Bi-parametric prostate MR image synthesis using pathology and sequence-conditioned stable diffusion.[[paper](https://arxiv.org/pdf/2303.02094)]|||||
|8|Cascaded Latent Diffusion Models for High-Resolution Chest X-ray Synthesis.[[paper](https://arxiv.org/pdf/2303.11224)]|||||
|9|DDMM-Synth: A Denoising Diffusion Model for Cross-modal Medical Image Synthesis with Sparse-view Measurement Embedding.[[paper](https://arxiv.org/pdf/2303.15770)]|||||
|10|Cycle-guided Denoising Diffusion Probability Model for 3D Cross-modality MRI Synthesis.[[paper](https://arxiv.org/pdf/2305.00042)]|||||
|11|Make-A-Volume: Leveraging Latent Diffusion Models for Cross-Modality 3D Brain MRI Synthesis.[[paper](https://arxiv.org/pdf/2307.10094)]|||||
|12|Noise-Consistent Siamese-Diffusion for Medical Image Synthesis and Segmentation.[[paper](https://arxiv.org/pdf/2505.06068)][[code](https://github.com/Qiukunpeng/Siamese-Diffusion.)]|arXiv,250509||||
|13|Guided synthesis of annotated lung CT images with pathologies using a multi-conditioned denoising diffusion probabilistic model (mDDPM).[[paper](https://iopscience.iop.org/article/10.1088/1361-6560/adb9b3/pdf)]| Physics in Medicine & Biology,20250306||CT|lung|
|14|Contrastive Diffusion Model with Auxiliary Guidance for Coarse-to-Fine PET Reconstruction.[[paper](https://doi.org/10.1007/978-3-031-43999-5_23)][[code](https://github.com/Show-han/PET-Reconstruction )]|MICCAI 2023||||
|15|Diffusion-based conditional ECG generation with structured state space models.[[paper](https://doi.org/10.1016/j.compbiomed.2023.107115)][[code](https://github.com/AI4HealthUOL/SSSD-ECG )]|Comput Biol Med 2023||||
|16|.[[paper]()][[code]()]|  ||||

### 1.4 Mamba-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|I2I-Mamba: Multi-modal medical image synthesis via selective state space modeling.[[paper](https://arxiv.org/abs/2405.14022)][[code](https://github.com/icon-lab/I2I-Mamba)]| |[[BrainMRI:IXI](https://brain-development.org/ixi-dataset/)] [[PelvisCT-MRI](https://zenodo.org/records/583096)]| MRI(T1,T2,PD) & MRI(T2w)->CT|Brain & Pelvis|
|2|MedMaskDiff: Mamba-Based Medical Semantic  Image Synthesis for Segmentation.[[paper](https://link.springer.com/chapter/10.1007/978-981-95-0030-7_16)][[code](https://github.com/Jiacheng-Han/MedMaskDiff)]|Advanced Intelligent Computing Technology and Applications，20250725||||
|3|Hierarchical multi-scale Mamba generative adversarial network for multi-modal medical image synthesis.[[paper](https://www.sciencedirect.com/science/article/pii/S0957417425010735)][[code](https://github.com/jlw9999/HMSMambaGAN)]|Expert Systems with Applications,20250625|||
|4|VM-DDPM: Vision Mamba Diffusion or Medical Image Synthesis.[[paper](https://arxiv.org/pdf/2405.05667)]|arXiv, 20240509||||
|5|.[[paper]()][[code]()]|||||
|6|.[[paper]()][[code]()]|||||

### 1.5 diffusion+transformer
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|3D Nephrographic Image Synthesis in CT Urography with the Diffusion Model and Swin Transformer.[[paper](https://arxiv.org/pdf/2502.19623)]|arXiv,20250226|||kidney|
|2|.[[paper]()][[code]()]|||||
|3|.[[paper]()][[code]()]|||||
|4|.[[paper]()][[code]()]|||||
|5|.[[paper]()][[code]()]|||||
|6|.[[paper]()][[code]()]|||||
|7|.[[paper]()][[code]()]|||||
|8|.[[paper]()][[code]()]|||||
|9|.[[paper]()][[code]()]|||||
|10|.[[paper]()][[code]()]|||||





## 2 Image-Translation
### 2.1 gan-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Multi-resolution Guided 3D GANs for Medical Image Translation[[paper](https://ieeexplore.ieee.org/abstract/document/10944137)][[code](https://github.com/juhha/3D-mADUNet)]|WACV 2025|HCP1200，dHCP，BraTS 2021，SynthRAD2023|T1/ T2/ Flair MRIs, CBCT, CT|brain,pelvis|
|2|PIX2PIX:Image-to-Image Translation with Conditional Adversarial Networks.[[paper](https://arxiv.org/pdf/1611.07004)][[code](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/README.md)]|CVPR2017||||
|3|TarGAN: Target-Aware Generative Adversarial Networks for Multi-modality Medical Image Translation[[paper](https://link.springer.com/chapter/10.1007/978-3-030-87231-1_3)][[code](https://github.com/cs-xiao/TarGAN)]|MICCAI 2021|Combined Healthy Abdominal Organ Segmentation (CHAOS)|CT,T1,T2|abdominal organs|
|4|CycleGAN:Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks.[[paper](https://arxiv.org/pdf/1703.10593)][[code](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/README.md)]|ICCV2017||||
|5|Swin transformer-based GAN for multi-modal medical image translation[[paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC9395186/)]|Frontiers in Oncology, 2022|BraTs2018, fastMRI|T1->T2,PD->PD-FS|Brain, Knee|
|6|Structure-Enhanced Translation from PET to CT Modality with Paired GANs[[paper](https://dl.acm.org/doi/abs/10.1145/3589572.3589593)]|ICMVA 2023|QIN-Brest|PET->CT|Brest|
|7|Compensation cycle consistent generative adversarial networks (Comp-GAN) for synthetic CT generation from MR scans with truncated anatomy[[paper](https://aapm.onlinelibrary.wiley.com/doi/abs/10.1002/mp.16246)]|Medical physics. 2023||MR->CT||
|8|Development of an unsupervised cycle contrastive unpaired translation network for MRI-to-CT synthesis[[paper](https://aapm.onlinelibrary.wiley.com/doi/full/10.1002/acm2.13775)]|Journal of Applied Clinical Medical Physics. 2022||MR->CT|Brain|
|9|DTR-GAN: An Unsupervised Bidirectional Translation Generative Adversarial Network for MRI-CT Registration[[paper](https://www.mdpi.com/2076-3417/14/1/95)]|Applied Sciences 2023|Learn2Reg, CHAOS|MRI<->CT|abdomen|
|10|Paired-unpaired unsupervised attention guided GAN with transfer learning for bidirectional brain MR-CT synthesis[[paper](https://www.sciencedirect.com/science/article/pii/S0010482521005576)]|Computers in Biology and Medicine. 2021|JUH dataset https://dx.doi.org/10.21227/fe9x-qg64|MR<->CT|Brain|
|11|CT synthesis from MRI using multi-cycle GAN for head-and-neck radiation therapy[[paper](https://www.sciencedirect.com/science/article/pii/S0895611121001026)]|Computerized medical imaging and graphics. 2021||MR->CT|head-and-neck|
|12|MedGAN: Medical image translation using GANs[[paper](https://www.sciencedirect.com/science/article/pii/S0895611119300990)|Computerized medical imaging and graphics, 2020||PET->CT|Brain|
|13|An Indirect Multimodal Image Registration and Completion Method Guided by Image Synthesis[[paper](https://onlinelibrary.wiley.com/doi/full/10.1155/2020/2684851)]|Computational and mathematical methods in medicine. 2020||MRI->CT|Head neck|
|14|High-quality PET image synthesis from ultra-low-dose PET/MRI using bi-task deep learning[[paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC9703111/)]|Quantitative Imaging in Medicine and Surgery. 2022 ||ultra-low-dose state->high-quality PET images|Head|
|15|Contrastive image adaptation for acquisition shift reduction in medical imaging[[paper](https://www.sciencedirect.com/science/article/pii/S0933365723002610)]|Artificial Intelligence in Medicine. 2024||MRI->CT|Brain|
|16|Multi-category domain-dependent feature-based medical image translation[[paper](https://link.springer.com/article/10.1007/s00371-023-03096-2)]|The Visual Computer. 2024|BRATS2015|T1<->T2|Brain|
|17|Structural attention: Rethinking transformer for unpaired medical image synthesis[[paper](https://link.springer.com/chapter/10.1007/978-3-031-72104-5_66)][[code](https://github.com/HieuPhan33/MICCAI2024-UNest)]|MICCAI 2024|MRXFDG, AutoPET|MRI->CT, MRI->PET, PET->CT|Brain, whole body(two different tasks)|
|18|CT-Based Pelvic T1-Weighted MR Image Synthesis Using UNet, UNet++ and Cycle-Consistent Generative Adversarial Network (Cycle-GAN)[[paper](https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2021.665807/full)]|Frontiers in oncology. 2021||CT->MR|Pelvis|
|19|Lumbar spine computed tomography to magnetic resonance imaging synthesis using generative adversarial network: Visual turing test[[paper](https://www.mdpi.com/2075-4418/12/2/530)]|Diagnostics. 2022||CT->MR|lumbar|
|20|Synthetic MRI generation from CT scans for stroke patients[[paper](https://www.mdpi.com/2673-7426/3/3/50)]|BioMedInformatics. 2023||CT->MR|Brain|
|21|Structure-preserving image translation for multi-source medical image domain adaptation[[paper](https://www.sciencedirect.com/science/article/pii/S0031320323005381)]|Pattern Recognition 2023||CT<->MR|Eye Fundus|
|22|ICycle-GAN: Improved cycle generative adversarial networks for liver medical image generation[[paper](https://www.sciencedirect.com/science/article/pii/S1746809424001587)]|Biomedical Signal Processing and Control. 2024|LiTS, CHAOS|CT<->MR|Liver|
|23|CT to MRI Image Translation Using CycleGAN: A Deep Learning Approach for Cross-Modality Medical Imaging.[[paper](https://www.scitepress.org/Papers/2024/124229/124229.pdf)]|InICAART (3) 2024||CT->MR|Brain|
|24|MRI cross-modality image-to-image translation[[paper](https://www.nature.com/articles/s41598-020-60520-6)]|Scientific Reports 2020|BraTs2015, Iseg2017, MRBrain13, ADNI, RIRE|T1<->T2, T1<->T2-flair, T2<->T2-flair|Brain|
|25|Cross-modality image translation: CT image synthesis of MR brain images using multi generative network with perceptual supervision[[paper](https://www.sciencedirect.com/science/article/pii/S0169260723002365)]|Computer Methods and Programs in Biomedicine. 2023||MRI<->CT|MRI|
|26|Multi-modal modality-masked diffusion network for brain mri synthesis with random modality missing[[paper](https://ieeexplore.ieee.org/abstract/document/10444695)]|IEEE Transactions on Medical Imaging 2024|BraTS, ProstateX, RaFD|Intra MRI|Brain, Prostate|
|27|Unified multi-modal image synthesis for missing modality imputation[[paper](https://ieeexplore.ieee.org/abstract/document/10589432)]|IEEE Transactions on Medical Imaging 2024|BraTS, IXI|Intra MRI|Brain|
|28|Hi-net: hybrid-fusion network for multi-modal MR image synthesis[[paper](https://ieeexplore.ieee.org/abstract/document/9004544)]|IEEE transactions on medical imaging. 2020|BraTs2018|T1 + T2 → Flair, T1 + Flair → T2, T2 + Flair → T1|Brain|

### 2.2 diffusion-based
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Cross-conditioned Diffusion Model for Medical Image to Image Translation.[[paper](https://arxiv.org/abs/2409.08500)][[code]()]|MICCAI, 2024||||
|2|Slice-Consistent 3D Volumetric Brain CT-to-MRI Translation with 2D Brownian Bridge Diffusion Model.[[paper](https://arxiv.org/abs/2407.05059)][[code](https://github.com/MICV-yonsei/CT2MRI)]|MICCAI, 2024||||
|3|2.5D Multi-view Averaging Diffusion Model for 3D Medical Image Translation: Application to Low-count PET Reconstruction with CT-less Attenuation Correction.[[paper](https://arxiv.org/abs/2406.08374)][[code]()]|||||
|4|Similarity-aware Syncretic Latent Diffusion Model for Medical Image Translation with Representation Learning.[[paper](https://arxiv.org/abs/2406.13977)][[code]()]|||||
|5|Cascaded Multi-path Shortcut Diffusion Model for Medical Image Translation.[[paper](https://arxiv.org/abs/2405.12223)][[code]()]|||||
|6|Diffusion based Zero-shot Medical Image-to-Image Translation for Cross Modality Segmentation.[[paper](https://arxiv.org/abs/2404.01102)][[code]()]|||||
|7|Self-Consistent Recursive Diffusion Bridge for Medical Image Translation.[[paper](https://arxiv.org/abs/2405.06789)][[code](https://github.com/icon-lab/SelfRDB)]|||||
|8|Tackling Structural Hallucination in Image Translation with Local Diffusion.[[paper](https://arxiv.org/abs/2404.05980)][[code]()]|||||
|9|ContourDiff: Unpaired Image Translation with Contour-Guided Diffusion Models.[[paper](https://arxiv.org/abs/2403.10786)][[code]()]|||||
|10|FDDM: Unsupervised Medical Image Translation with a Frequency-Decoupled Diffusion Model.[[paper](https://arxiv.org/abs/2311.12070)][[code]()]|||||
|11|Adaptive Latent Diffusion Model for 3D Medical Image to Image Translation: Multi-modal Magnetic Resonance Imaging Study.[[paper](https://arxiv.org/abs/2311.00265)][[code](https://github.com/jongdory/ALDM/)]|WACV, 2024||||
|12|Cycle-guided Denoising Diffusion Probability Model for 3D Cross-modality MRI Synthesis.[[paper](https://arxiv.org/abs/2305.00042)][[code]()]|arXiv, 2023||||
|13|Zero-shot Medical Image Translation via Frequency-Guided Diffusion Models.[[paper](https://arxiv.org/abs/2304.02742)][[code](https://github.com/Kent0n-Li/FGDM)]|arXiv, 2023||||
|14|Zero-shot-Learning Cross-Modality Data Translation Through Mutual Information Guided Stochastic Diffusion.[[paper](https://arxiv.org/abs/2301.13743)][[code]()]|arXiv, 2023||||
|15|Unsupervised Medical Image Translation with Adversarial Diffusion Models.[[paper](https://arxiv.org/abs/2207.08208)][[code]()]|IEEE TMI Journal, 2022||||
|16|Target-guided diffusion models for unpaired cross-modality medical image translation[[paper](https://ieeexplore.ieee.org/abstract/document/10508481)]|Journal of Biomedical and Health Informatics. 2024||MRI-CT,MRI-US|Brain, Prostate|
|17|Diffusion-based domain adaptation for medical image segmentation using stochastic step alignment[[paper](https://link.springer.com/chapter/10.1007/978-3-031-72111-3_18)]|MICCAI 2024|CHAOS, BTCV|MR<->CT|abdomen|
|18|Adaptive latent diffusion model for 3d medical image to image translation: Multi-modal magnetic resonance imaging study[[paper](https://openaccess.thecvf.com/content/WACV2024/html/Kim_Adaptive_Latent_Diffusion_Model_for_3D_Medical_Image_to_Image_WACV_2024_paper.html)][[code](https://github.com/jongdory/ALDM/)]|WACV 2024|BraTS 2021, IXI dataset|T1->T2, T2->FLAIR, T1->PD|Brain|
|19|Disentangle and Then Fuse: A Cross-Modal Network for Synthesizing Gadolinium-Enhanced Brain MR Images[[paper](https://ieeexplore.ieee.org/abstract/document/10839402)]|IEEE Transactions on Circuits and Systems for Video Technology. 2025|BRaTS2020, BRaTS2021, Private HPPH|Gadolinium-Enhanced?|Brain|
|20|Fast-DDPM: Fast Denoising Diffusion Probabilistic Models for Medical Image-to-Image Generation[[paper](https://ieeexplore.ieee.org/abstract/document/10979336)][[code](https://github.com/mirthAI/Fast-DDPM)]|IEEE Journal of Biomedical and Health Informatics. 2025 |BraTS 2018|T1w->T2w|Brain|
|21|Make-a-volume: Leveraging latent diffusion models for cross-modality 3d brain mri synthesis[[paper](https://link.springer.com/chapter/10.1007/978-3-031-43999-5_56)]|MICCAI 2023|SWI-to-MRA, RIRE|T1->T2|Brain|
|22|Cola-diff: Conditional latent diffusion model for multi-modal mri synthesis[[paper](https://link.springer.com/chapter/10.1007/978-3-031-43999-5_38)][[code](https://github.com/SeeMeInCrown/CoLa Diﬀ MultiModal MRI Synthesis)]|MICCAI 2023|BRATS 2018, IXI|Translation between T2, T1ce, T1 and Flair|Brain|
|23|Cross-domain super-resolution in medical imaging[[paper](https://ieeexplore.ieee.org/abstract/document/10733648)]|ISCC 2024 |Automatic Cardiac Diagnosis Challenge (ACDC), OpenImages|Low-resolution → High-resolution(MR)|Heart, Brain, Hand, Thoraxes|
|24|Wdm: 3d wavelet diffusion models for high-resolution medical image synthesis[[paper](https://link.springer.com/chapter/10.1007/978-3-031-72744-3_2)][[code](https://pfriedri.github.io/wdm-3d-io)]|MICCAI workshop on deep generative models 2024|BraTS 2023, LIDC-IDRI|Low-Resolution → High-resolution|Brain, Lung|
|25|Conversion Between CT and MRI Images Using Diffusion and Score-Matching Models[[paper](https://arxiv.org/abs/2209.12104)]|arXiv:2209.12104 (2022)|Gold Atlas male pelvis dataset|MRI → CT|pelvis|
|26|2D medical image synthesis using transformer-based denoising diffusion probabilistic model[[paper](https://iopscience.iop.org/article/10.1088/1361-6560/acca5c/meta)]|Physics in Medicine & Biology. 2023|NIH Chest x-rays dataset, Automated Cardiac Diagnosis Challenge (ACDC), Beyond the Cranial Vault (BTCV)|||
|27|Boundary information‐guided adversarial diffusion model for efficient unsupervised synthetic CT generation[[paper](https://aapm.onlinelibrary.wiley.com/doi/abs/10.1002/mp.17723)]|Medical Physics. 2025||||
|28|Multi-Modal Modality-Masked Diffusion Network for Brain MRI Synthesis With Random Modality Missing[[paper](https://ieeexplore.ieee.org/abstract/document/10444695)]|IEEE Transactions on Medical Imaging 2024|IXI, BraTS-2019|Arbitrary-modality brain MRI synthesis|Brain|
|29|.[[paper]()][[code]()]|||||
|30|.[[paper]()][[code]()]|||||



### mamba-diffusion
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Soft Masked Mamba Diffusion Model for CT to MRI Conversion.[[paper](https://arxiv.org/abs/2406.15910)][[code](https://github.com/wongzbb/DiffMa-Diffusion-Mamba)]|||||
|2|I2I-Mamba: Multi-modal medical image synthesis via selective state space modeling[[paper](https://arxiv.org/abs/2405.14022)]|arXiv 2024|IXI, BraTS, multi-modal pelvic MRI-CT dataset|Translation among T1, T2, Flair, PD|Brain, Plevis|
|3|.[[paper]()][[code]()]|||||
|4|.[[paper]()][[code]()]|||||
|5|.[[paper]()][[code]()]|||||
|6|.[[paper]()][[code]()]|||||
|7|.[[paper]()][[code]()]|||||
|8|.[[paper]()][[code]()]|||||
|9|.[[paper]()][[code]()]|||||
|10|.[[paper]()][[code]()]|||||



## others_image_translation
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 | Method |
|---------|---------|---------|---------|---------|---------|---------|
|1|Mitigating analytical variability in fMRI results with style transfer.[[paper](https://arxiv.org/abs/2404.03703)][[code]()]||||||
|2|Class-Guided Image-to-Image Diffusion: Cell Painting from Brightfield Images with Class Labels.[[paper](https://arxiv.org/abs/2303.08863)][[code](https://github.com/crosszamirski/guided-I2I)]|arXiv, 2023|||||
|3|Diffusion Models for Contrast Harmonization of Magnetic Resonance Images.[[paper](https://arxiv.org/abs/2303.08189)][[code]()]|MIDL, 2023|||||
|4|Conversion Between CT and MRI Images Using Diffusion and Score-Matching Models.[[paper](https://arxiv.org/abs/2209.12104)][[code]()]|arXiv, 2022|||||
|5|A Novel Unified Conditional Score-based Generative Framework for Multi-modal Medical Image Completion.[[paper](https://arxiv.org/abs/2207.03430)][[code]()]|arXiv, 2022|||||
|6|SARU: A self-attention ResUNet to generate synthetic CT images for MR-only BNCT treatment planning[[paper](https://aapm.onlinelibrary.wiley.com/doi/abs/10.1002/mp.15986)]|Medical Physics. 2023||MRI → CT|Brain|self-attention ResUnet|
|7|MRI-based synthetic CT in the detection of knee osteoarthritis: Comparison with CT[[paper](https://onlinelibrary.wiley.com/doi/full/10.1002/jor.25557)]|Journal of Orthopaedic Research. 2023||MRI → CT|Knee|3D U-Net|
|8|Deep learning for synthetic CT from bone MRI in the head and neck[[paper](https://www.ajnr.org/content/43/8/1172.abstract)]|American Journal of Neuroradiology. 2022||MRI → CT|Head neck|Light U-Net, VGG-16 U-Net|
|9|Medprompt: Cross-modal prompting for multi-task medical image translation[[paper](https://link.springer.com/chapter/10.1007/978-981-97-8496-7_5)]|Chinese Conference on Pattern Recognition and Computer Vision (PRCV) 2024|ADNI, SynthRAD2023, IXI, BraTS2020|Translation between T1 and T2|Brain|Transformer|
|10|MRNet: Multifaceted Resilient Networks for Medical Image-to-Image Translation[[paper](https://arxiv.org/abs/2412.03039)]|arXiv 2024|SynthRAD2023, Brats|MRI->CT|Brain|SAM-Based|
|11|Boundary information‐guided adversarial diffusion model for efficient unsupervised synthetic CT generation[[paper](https://aapm.onlinelibrary.wiley.com/doi/abs/10.1002/mp.17723)]|Medical Physics. 2025||MRI->CT|Plevis|Diffusion-GAN|
|12|One Model to Synthesize Them All: Multi-Contrast Multi-Scale Transformer for Missing Data Imputation[[paper](https://ieeexplore.ieee.org/abstract/document/10081095)]|IEEE transactions on medical imaging|IXI，BraTS 2021|Intra MRI|Brain|Transformer|
|13|.[[paper]()][[code]()]||||||
|14|.[[paper]()][[code]()]||||||
|15|.[[paper]()][[code]()]||||||

## 3 image fusion
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|DDFM: Denoising Diffusion Model for Multi-Modality Image Fusion.[[paper](https://arxiv.org/pdf/2303.06840)][[code](https://github.com/Zhaozixiang1228/MMIF-DDFM)]|ICCV23 Oral||||
|2|LFDT-Fusion: A latent feature-guided diffusion Transformer model for general image fusion.[[paper](https://www.sciencedirect.com/science/article/pii/S1566253524004172)]|Information Fusion 2025||||
|3|DCFFSNet: Deep Connectivity Feature Fusion Separation Network for Medical Image Segmentation.[[paper](https://arxiv.org/abs/2507.18407)]|arXiv，2025||||
|4|MedSAM-CA:mentation A CNN-Augmented ViT with Attention-Enhanced Multi-Scale Fusion for Medical Image Segmentation.[[paper](https://arxiv.org/abs/2506.23700)]|arXiv，2025||||
|5|UniFuse: A Unified All-in-One Framework for Multi-Modal Medical Image Fusion Under Diverse Degradations and Misalignments.[[paper](https://arxiv.org/abs/2506.22736)][[code]()]|arXiv，2025||||
|6|MedPrompt: LLM-CNN Fusion with Weight Routing for Medical Image Segmentation and Classification.[[paper](https://arxiv.org/abs/2506.21199)]|arXiv，2025||||
|7|AMF-MedIT: An Efficient Align-Modulation-Fusion Framework for Medical Image-Tabular Data.[[paper](https://arxiv.org/abs/2506.19439)]|arXiv，2025||||
|8|Adversarial robust image processing in medical digital twin.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253524005062)]|Information Fusion 2025||||
|9|OmniFuse: A general modality fusion framework for multi-modality learning on low-quality medical data.[[paper](https://www.sciencedirect.com/science/article/pii/S1566253524006687#:~:text=To%20fully%20harness%20the%20potential%20of%20multi-modal%20low-quality,challenges%20on%20varying%20medical%20scenarios%20involving%20multiple%20modalities.)]|Information Fusion 2025||||
|10|DAFNet: A novel Dynamic Adaptive Fusion Network for medical image classification.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253525005792)]|Information Fusion 2025||||
|11|Entropy-aware dynamic path selection network for multi-modality medical image fusion.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253525003859)]|Information Fusion 2025||||
|12|Vision-Language Models in medical image analysis: From simple fusion to general large models.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253525000685)][[code](https://github.com/XiangQA-Q/VLM-in-MIA)]|Information Fusion 2025||||
|13|LPM-Net: Lightweight pixel-level modeling network based on CNN and Mamba for 3D medical image fusion.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253525003793)][[code](https://github.com/coolllcat/LPM-Net)]|Information Fusion 2025||||
|14|OmniFuse: A general modality fusion framework for multi-modality learning on low-quality medical data.[[paper](https://www.sciencedirect.com/science/article/pii/S1566253524006687)]|Information Fusion 2025||||
|15|SSEFusion: Salient semantic enhancement for multimodal medical image fusion with Mamba and dynamic spiking neural networks.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253525001046)][[code](https://github.com/Shiqiang-Liu/SSEFusion)]|Information Fusion 2025||||
|16|Multimodal Fusion Learning with Dual Attention for Medical Imaging.[[paper](https://arxiv.org/abs/2412.01248)][[code]()]|arXiv，2025||||
|17|MMIF-INet: Multimodal medical image fusion by invertible network.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253524004445)][[code](https://github.com/HeDan-11/MMIF-INet)]|Information Fusion 2025||||
|18|Medical image super-resolution for smart healthcare applications: A comprehensive survey.[[paper](https://www.sciencedirect.com/science/article/pii/S1566253523003913)]|Information Fusion 2025||||
|19|DM-FNet: Unified multimodal medical image fusion via diffusion process-trained encoder-decoder.[[paper](https://arxiv.org/abs/2506.15218)][[code](https://github.com/HeDan-11/DM-FNet)]|TMM 2025||||
|20|Advancing multimodal medical image fusion: an adaptive image decomposition approach based on multilevel Guided filtering.[[paper](https://royalsocietypublishing.org/doi/10.1098/rsos.231762)]|ROYAL SOCIETY OPEN SCIENCE 2024||||
|21|Simultaneous tri-modal medical image fusion and super-resolution using conditional diffusion model.[[paper](https://arxiv.org/abs/2404.17357)][[code](https://github.com/XylonXu01/TFS-Diff)]|MICCAI 2024||||
|22|Medical image fusion with deep neural networks.[[paper](https://www.nature.com/articles/s41598-024-58665-9)]|Scientific Reports 2024||||
|23|Medical image fusion: A survey of the state of the art.[[paper](https://pdf.sciencedirectassets.com/272144/1-s2.0-S1566253514X00023/1-s2.0-S1566253513001450/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEPb%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJGMEQCIFSblswro6NOny2eHY8wOIdFCs8zr6ArK9dIRGHj9Zp7AiAQ9T%2FJG6g5Vwao9fTkSQ7eWnWJnh6J005Jgz40mbPR%2BSqzBQgfEAUaDDA1OTAwMzU0Njg2NSIMXRoLwZjNoBgEzBpcKpAFPwzhPcR6FbtWMIUsKGQdXFuPPkzUd2odEoz%2BwGMSUL4P%2FPrGdV7h5Qn6ojyGVR5j7MR6zNjUpQTiyb9J%2F5doKQB%2FOKS%2F1LhKHvlRKeiZGtMInnuLyfrAZqBkOxFohbhP10mk8OjjIs%2F67GMw%2BamEkAbHBQacdNy14d5MrvBCxRKUMfZHpQVto7hW8sFrlsSEDkuc1pnBzoVxw7bIdX5uYgKZ965uPUvKXqXx1rnSg6A1%2FOGwC1n9C7Aco33th%2BkZo68Xg0pTf57NBvzVxtu81UY8J6prbgpB5pGtY66OvPyc7DqBRSs8XBvRnhnp3QNeln9XZnBZgiCsAbwSJleWcGof5gx1i2YUmWPu5U00yn%2BGo%2BmVb4ZwCxX2q3%2BeOo3z6in6F3vPtXWIYujwPO8TvovtPCdT8Hsd1W0iuOhnzUdKU0SdjKlvLSpOKNBzdeXGLDKF8Bjls6B301mgbvIVdeuRvkHZGftwAsKSyX6tEEaN0RtrfrtJWbUEek%2Bc8S6NWXZVUB4ZRQGl1L2r6wgajUVfznFu%2BBeUKVbLkLKiSO%2BbwCmwOI3wsh%2BmUb%2FgFMAgUACdXKw4H7ZU4tU1YBQlFQIDxm7fs75kyRLR%2F0zbSKCXZVk1yTJnuauOJX0WNHzR4dSqtSCqKTASqvAqXDsnDQGj027%2F4yMuDplK5nDEA6uEagroWNkSVZ6QOPBRnwpA6YF7f6S%2B9cFUNPUUXnirFXq%2FjfRIO553XL7xRxMpv7%2FztWmr%2Fs%2Feqksz%2BcACHowG3CRbi3RwgPg1nlYt45pqaMX%2Bc5AsDOZ1FTlh5XGJWnVpk5389xvjvdzanakWuthChpdy9DH7qgwoRD7cj9IH8CjNXdj2eScEDf%2FkQaeUA30whq2FxAY6sgH6vmWnN9tlG5IAdiv0thO5l%2BThdoTaiRgMqm%2F1wSvdgWI%2FsM1OJYU%2BzY9%2FmdcrliUZlguieimDu9oVFJeGqRyVXnT6XVctRGQqH41uasSe6z9BE8j5rs6GlMBvcYM8VNdnZvthcIhdh1It%2FZPGe9KybzK%2BlEgrrtBGrqYVl%2Fm9S%2B5h1HraG5Ht9N1SwETbqjL4YbzgdCRxMegun3FNTy8payFghEzubu3ls22InQbGqqOT&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20250723T220110Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYZMAMDVHK%2F20250723%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=b94cc9c2524e77d5ab5c88adc2fc34cd98f1a948493de04def05977a5714cbe2&hash=c597026fdf1d26e2ff05258d0c772738e6f9e382ee68d71374ef369a10f901ce&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S1566253513001450&tid=spdf-d86eebfb-624f-462a-a98b-473c0f0375b5&sid=6142a02e9278d94d80087fc936726e8b4fdcgxrqb&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&rh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=1d045b585c01575354&rr=963e7471fc290f12&cc=gb)][[code]()]|Information Fusion 2014||||

## 4 image generation
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Medical Diffusion: Denoising Diffusion Probabilistic Models for 3D Medical Image Generation.[[paper](https://arxiv.org/pdf/2211.03364)][[code](https://github.com/FirasGit/medicaldiffusion)]||||MR:Knee breast brain CT:thoracic|
|2|Fast-DDPM: Fast Denoising Diffusion Probabilistic Models for Medical Image-to-Image Generation.[[paper](https://arxiv.org/abs/2405.14802)][[code](https://github.com/mirthAI/Fast-DDPM)]|||||
|3|Fast-DDPM: Fast Denoising Diffusion Probabilistic Models for Medical Image-to-Image Generation.[[paper](https://arxiv.org/abs/2405.14802)][[code](https://github.com/mirthAI/Fast-DDPM)]|arXiV 2024 05 24||||
|4|Accelerating Medical Evidence Generation and Use: Summary of a Meeting Series.[[paper](https://nap.nationalacademies.org/catalog/27123/accelerating-medical-evidence-generation-and-use-summary-of-a-meeting)][[code]()]|NATIONAL ACADEMIES 2023 ||||
|5|Medical Image Generation Using Generative Adversarial Networks: A Review.[[paper](https://link.springer.com/chapter/10.1007/978-981-15-9735-0_5)][[code]()]|Springer Nature 2021 01 31||||
|6|Denoising diffusion probabilistic models for 3D medical image generation.[[paper](https://www.nature.com/articles/s41598-023-34341-2)][[code]()]|Scientific Reports 2023 05 05||||
|7|Med-cDiff: Conditional Medical Image Generation with Diffusion Models.[[paper](https://www.mdpi.com/2306-5354/10/11/1258)][[code]()]|MDPI 2023 10 28||||
|8|MedGAN: An adaptive GAN approach for medical image generation.[[paper](https://www.sciencedirect.com/science/article/abs/pii/S001048252300584X)][[code]( https://github.com/geyao-c/MedGAN)]|ScienceDirect 2023 09||||
|9|Deep learning for whole-body medical image generation.[[paper](https://link.springer.com/article/10.1007/s00259-021-05413-0)][[code]()]|Springer Nature 2021||||
|10|Self-improving generative foundation model for synthetic medical image generation and clinical applications.[[paper](https://www.nature.com/articles/s41591-024-03359-y)][[code]()]|Nature Medicine 2024 12 11||||
|11|MedSymmFlow: Bridging Generative Modeling and Classification in Medical Imaging through Symmetrical Flow Matching.[[paper](https://arxiv.org/abs/2507.19098)][[code](github.com/caetas/MedSymmFlow)]|arXiV 2025 07 25||||
|12|EndoGen: Conditional Autoregressive Endoscopic Video Generation.[[paper](https://arxiv.org/pdf/2507.17388)][[code](https://www.github.com/CUHK-AIM-Group/EndoGen)]|arXiV 2025 07 23||||
|13|OrthoInsight: Rib Fracture Diagnosis and Report Generation Based on Multi-Modal Large Models.[[paper](https://arxiv.org/abs/2507.13993)][[code]()]|arXiV 2025 07 18||||
|14|Pixel Perfect MegaMed: A Megapixel-Scale Vision-Language Foundation Model for Generating High Resolution Medical Images.[[paper](https://arxiv.org/abs/2507.12698)][[code](https://tehraninasab.github.io/pixelperfect-megamed/)]|arXiV 2025 07 17||||
|15|Diffusion Deformable Model for 4D Temporal Medical Image Generation.[[paper](https://link.springer.com/chapter/10.1007/978-3-031-16431-6_51)][[code]()]|google scholar 2022 09 15||||
|16|A New Chapter for Medical Image Generation: The Stable Diffusion Method.[[paper](https://ieeexplore.ieee.org/abstract/document/10049010)][[code]()]|IEEE 2023 02 22||||
|17|SADM: Sequence-Aware Diffusion Model for Longitudinal Medical Image Generation.[[paper](https://link.springer.com/chapter/10.1007/978-3-031-34048-2_30)][[code]( https://github.com/ubc-tea/SADM-Longitudinal-Medical-Image-Generation.)]|google scholar 2023 06 08||||
|18|Medical diffusion on a budget: Textual Inversion for medical image generation.[[paper](https://arxiv.org/abs/2303.13430)][[code](https://github.com/brambozz/medical-diffusion-on-a-budget)]|arXiV 2024 09 11||||
|19|Conditional GAN with an Attention-Based Generator and a 3D Discriminator for 3D Medical Image Generation.[[paper](https://link.springer.com/chapter/10.1007/978-3-030-87231-1_31)][[code]()]|Springer Nature 2021 09 21||||
|20|Multi-Modal Understanding and Generation for Medical Images and Text via Vision-Language Pre-Training.[[paper](https://ieeexplore.ieee.org/abstract/document/9894658)][[code]()]|IEEE 2022 09 19||||
|21|Fast and low-dose medical imaging generation empowered by hybrid deep-learning and iterative reconstruction.[[paper](https://www.cell.com/cell-reports-medicine/fulltext/S2666-3791(23)00247-1?uuid=uuid%3Ab74b448b-1e67-4b8c-acc4-4ebe41c1d258)][[code]()]|Cell Reports Medicine  2023 07 18||||

## 5 image restoration
### 5.0 general restoration
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Restore-RWKV: Efficient and Effective Medical Image Restoration with RWKV.[[paper](https://arxiv.org/pdf/2407.11087)][[code](https://github.com/Yaziwel/Restore-RWKV)]|arxiv20250106||||
|2|Research on GAN-based MII-Net spine x-ray image restoration model in medical images.[[paper](https://doi.org/10.1117/12.3035461)]|||||
|3|R2C-GAN: Restore-to-Classify Generative Adversarial Networks for blind X-ray restoration and COVID-19 classification.[[paper](https://doi.org/10.1016/j.patcog.2024.110765)]|||||
|4|Endoir: A GAN-based method for fiber bundle endoscope image restoration.[[paper](https://doi.org/10.1016/j.optlaseng.2024.108588)]|||||
|5|Versatile Cataract Fundus Image Restoration Model Utilizing Unpaired Cataract and High-quality Images.[[paper](https://doi.org/10.1038/s41598-025-88444-z)]|arXiv,20241119||||
|6|Echocardiography to Cardiac MRI View Transformation for Real-Time Blind Restoration.[[paper](https://arxiv.org/abs/2412.06445)]|arXiv,20241209||||
|7|
|8|
|9|
|10|
|11|
|12|
|13|
|14|
|15|
|16|
|17|
|18|
|19|
|20|
|21|
|22|


### 5.1 inpainting
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Multitask Brain Tumor Inpainting with Diffusion Models: A Methodological Report.[[paper](https://arxiv.org/abs/2210.12113)][code](https://github.com/Mayo-Radiology-Informatics-Lab/MBTI)]|arXiv,20221021||||
|2|MaskMedPaint: Masked Medical Image Inpainting with Diffusion Models for Mitigation of Spurious Correlations.[[paper](http://arxiv.org/abs/2411.10686v1)][code](https://github.com/QixuanJin99/generative_validation)]|ML4H,20241116||||
|3|Investigating the Role of Bilateral Symmetry for Inpainting Brain MRI.[[paper](http://arxiv.org/abs/2504.10039v1)]|arXiv,20250414||||
|4|FCDM: Sparse - view Sinogram Inpainting with Frequency Domain Convolution Enhanced Diffusion Models.[[paper](https://arxiv.org/abs/2409.06714)]|arXiv,20240826||||
|5|Inpainting Pathology in Lumbar Spine MRI with Latent Diffusion.[[paper](https://arxiv.org/abs/2406.02477)]|arXiv,20240604||||






### 5.2 Super Resolution
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Transformer and GAN Based Super-Resolution Reconstruction Network for Medical Images.[[paper](https://arxiv.org/abs/2212.13068)]|arXiv,20221126||||
|2|A new generative adversarial network for medical images super resolution.[[paper](https://doi.org/10.1038/s41598-022-13658-4)]|nature,20220617||||
|5|MRI super-resolution reconstruction using efficient diffusion probabilistic model with residual shifting.[[paper](http://arxiv.org/abs/2503.01576v2)][[code](https://github.com/mosaf/Res-SRDiff)]|arXiv, 20250303||||
|6|Implicit Image-to-Image Schrodinger Bridge for CT Super-Resolution and Denoising.[[paper](https://arxiv.org/abs/2403.06069)]|arXiv, 20240310||||
|7|Simultaneous Tri-Modal Medical Image Fusion and Super-Resolution using Conditional Diffusion Model.[[paper](https://arxiv.org/abs/2404.17357)]|arXiv, 20240426||||
|8|Image Compression and Decompression Framework Based on Latent Diffusion Model for Breast Mammography.[[paper](https://arxiv.org/abs/2310.05299)]|arXiv, 20231008||||
|9|Cas-DiffCom: Cascaded diffusion model for infant longitudinal super-resolution 3D medical image completion.[[paper](https://arxiv.org/abs/2402.13776)]|arXiv, 20240221||||
|10|DisC-Diff: Disentangled Conditional Diffusion Model for Multi-Contrast MRI Super-Resolution.[[paper](https://arxiv.org/abs/2303.13933)]|arXiv, 20230324||||
|11|InverseSR: 3D Brain MRI Super-Resolution Using a Latent Diffusion Model.[[paper](https://arxiv.org/abs/2308.12465)][[code](https://github.com/BioMedAI-UCSC/InverseSR)]|MICCAI, 20230823||||
|12|Self-similarity-based super-resolution of photoacoustic angiography from hand-drawn doodles.[[paper](https://arxiv.org/abs/2305.01165)][[code](https://github.com/yuanzhengthu/handDrawnPAAImages)]|arXiv, 20230502||||


### 5.3 denoising
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Objective and Interpretable Breast Cosmesis Evaluation with Attention Guided Denoising Diffusion Anomaly Detection Model.[[paper](https://arxiv.org/abs/2402.18362)]|arXive,20240228||||
|2|MCDDPM: Multichannel Conditional Denoising Diffusion Model for Unsupervised Anomaly Detection in Brain MRI.[[paper](https://arxiv.org/abs/2409.19623)][[code](https://github.com/vivekkumartri/MCDDPM)]|arXive,20240929||||
|3|Binary Noise for Binary Tasks: Masked Bernoulli Diffusion for Unsupervised Anomaly Detection.[[paper](https://arxiv.org/abs/2403.11667)][[code](https://github.com/JuliaWolleb/Anomaly_berdif)]|arXiv, 20240518||||
|4|The role of noise in denoising models for anomaly detection in medical images.[[paper](https://arxiv.org/abs/2301.08330)][[code](https://github.com/AntanasKascenas/DenoisingAE)]|arXiv,20230119||||
|5|AnoDDPM: Anomaly Detection with Denoising Diffusion Probabilistic Models using Simplex Noise.[[paper](https://openaccess.thecvf.com/content/CVPR2022W/NTIRE/papers/Wyatt_AnoDDPM_Anomaly_Detection_With_Denoising_Diffusion_Probabilistic_Models_Using_Simplex_CVPRW_2022_paper.pdf)][[code](https://github.com/Julian-Wyatt/AnoDDPM)]|CVPR Workshop, 20220601||||
|6|Ultrasound Imaging based on the Variance of a Diffusion Restoration Model.[[paper](https://arxiv.org/pdf/2403.15316)][[code](https://github.com/Yuxin-Zhang-Jasmine/DRUSvar)]|EUSIPCO,20240617||||
|7|Dose-aware Diffusion Model for 3D Low-dose PET: Multi-institutional Validation with Reader Study and Real Low-dose Data.[[paper](https://arxiv.org/abs/2405.12996)]|arXiv, 20240502||||
|8|Implicit Image-to-Image Schrodinger Bridge for CT Super-Resolution and Denoising.[[paper](https://arxiv.org/abs/2403.06069)]|arXiv, 20240510||||
|9|SDDPM: Speckle Denoising Diffusion Probabilistic Models.[[paper](https://arxiv.org/abs/2311.10868)][[code]()]|arXiv, 20231117||||
|10|Deep Ultrasound Denoising Using Diffusion Probabilistic Models.[[paper](https://arxiv.org/abs/2306.07440)][[code]()]|arXive,20230612||||
|11|A Diffusion Probabilistic Prior for Low-Dose CT Image Denoising.[[paper](https://arxiv.org/abs/2305.15887)]|arXive,20240525||||
|12|CoreDiff: Contextual Error-Modulated Generalized Diffusion Model for Low-Dose CT Denoising and Generalization.[[paper](https://arxiv.org/abs/2304.01814)]|arXiv, 20230404||||
|13|DDM2: Self-Supervised Diffusion MRI Denoising with Generative Diffusion Models.[[paper](https://arxiv.org/abs/2302.03018)][[code](https://github.com/StanfordMIMI/DDM2)]|arXive,20230206||||
|14|Low-Dose CT Using Denoising Diffusion Probabilistic Model for 20× Speedup.[[paper](https://arxiv.org/abs/2304.01814)]|arXiv, 2022092||||
|15|PET image denoising based on denoising diffusion probabilistic models.[[paper](https://arxiv.org/abs/2209.06167)]|European Journal of Nuclear Medicine and Molecular Imaging, 20220913||||
|16|Unsupervised Denoising of Retinal OCT with Diffusion Probabilistic Model.[[paper](https://arxiv.org/abs/2201.11760)][[code](https://github.com/DeweiHu/OCT_DDPM)]|Medical Imaging 2022: Image Processing,20220127||||
|17|MPGAN: Multi Pareto Generative Adversarial Network for the denoising and quantitative analysis of low-dose PET images of human brain.[[paper](https://doi.org/10.1016/j.media.2024.103306)][[code]()]|||||
|3|PET Image Denoising Based on 3D Denoising Diffusion Probabilistic Model Evaluations on Total‑Body Datasets.[[paper](https://doi.org/10.1007/978-3-031-72104-5_52)][[code]()]|arXive,20241003||||
|18|Denoising Diffusion Models for Anomaly Localization in Medical Images.[[paper](http://arxiv.org/abs/2410.23834v1)]|arXiv, 20241031||||
|19|MCDDPM: Multichannel Conditional Denoising Diffusion Model for Unsupervised Anomaly Detection in Brain MRI.[[paper](https://arxiv.org/abs/2409.19623)][[code](https://github.com/vivekkumartri/MCDDPM)]|arXiv, 20240929||||
|20|Binary Noise for Binary Tasks: Masked Bernoulli Diffusion for Unsupervised Anomaly Detection.[[paper](https://arxiv.org/abs/2403.11667)][[code](https://github.com/JuliaWolleb/Anomaly_berdif)]|arXiv, 20240313||||
|21|The role of noise in denoising models for anomaly detection in medical images.[[paper](https://arxiv.org/abs/2301.08330)][[code](https://github.com/AntanasKascenas/DenoisingAE)]|MedIA Journal, 20230119||||
|22|AnoDDPM: Anomaly Detection with Denoising Diffusion Probabilistic Models using Simplex Noise.[[paper](https://openaccess.thecvf.com/content/CVPR2022W/NTIRE/papers/Wyatt_AnoDDPM_Anomaly_Detection_With_Denoising_Diffusion_Probabilistic_Models_Using_Simplex_CVPRW_2022_paper.pdf)][[code](https://github.com/Julian-Wyatt/AnoDDPM)]|CVPR Workshop, 20220601||||
|23|DiffDenoise: Self - Supervised Medical Image Denoising with Conditional Diffusion Models.[[paper](http://arxiv.org/abs/2504.00264v1)]|arXiv, 20250331||||
|23|Ultrasound Imaging based on the Variance of a Diffusion Restoration Model.[[paper](https://arxiv.org/pdf/2403.15316)][[code](https://github.com/Yuxin-Zhang-Jasmine/DRUSvar)]|EUSIPCO, 20240617||||
|23|Dose - aware Diffusion Model for 3D Low - dose PET: Multi - institutional Validation with Reader Study and Real Low - dose Data.[[paper](https://arxiv.org/abs/2405.12996)]|arXiv, 20240502||||
|23|Implicit Image - to - Image Schrodinger Bridge for CT Super - Resolution and Denoising.[[paper](https://arxiv.org/abs/2403.06069)]|arXiv, 20240310||||
|23|SDDPM: Speckle Denoising Diffusion Probabilistic Models.[[paper](https://arxiv.org/abs/2311.10868)]|arXiv, 20231117||||
|23|Deep Ultrasound Denoising Using Diffusion Probabilistic Models.[[paper](https://arxiv.org/abs/2306.07440)]|arXiv, 20230612||||
|24|A Diffusion Probabilistic Prior for Low - Dose CT Image Denoising.[[paper](https://arxiv.org/abs/2305.15887)]|arXiv,20230525||||
|24|CoreDiff: Contextual Error - Modulated Generalized Diffusion Model for Low - Dose CT Denoising and Generalization.[[paper](https://arxiv.org/abs/2304.01814)]|arXiv,20230404||||
|24|DDM2: Self - Supervised Diffusion MRI Denoising with Generative Diffusion Models.[[paper](https://arxiv.org/abs/2302.03018)][[code](https://github.com/StanfordMIMI/DDM2)]|ICLR,20230206||||
|24|Low - Dose CT Using Denoising Diffusion Probabilistic Model for 20× Speedup.[[paper](https://arxiv.org/abs/2209.15136)]|arXiv,20220929||||
|24|PET image denoising based on denoising diffusion probabilistic models.[[paper](https://arxiv.org/abs/2209.06167)]|European Journal of Nuclear Medicine and Molecular Imaging,20220913||||
|24|Unsupervised Denoising of Retinal OCT with Diffusion Probabilistic Model.[[paper](https://arxiv.org/abs/2201.11760)][[code](https://github.com/DeweiHu/OCT_DDPM)]|Medical Imaging 2022: Image Processing,20220127||||
|23|Adaptive Whole-Body PET Image Denoising Using 3D Diffusion Models with ControlNet.[[paper](https://doi.org/10.48550/arXiv.2411.05302)]|arXive,20240908||||
|24|.[[paper]()][[code]()]|||||
|25|.[[paper]()][[code]()]|||||


### 5.4 Enhancement
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|
|2|Mask, Stitch, and Re-Sample: Enhancing Robustness and Generalizability in Anomaly Detection through Automatic Diffusion Models.[[paper](https://arxiv.org/abs/2305.19643)]|arXiv,20230531||||
|3|MAEDiff: Masked Autoencoder-enhanced Diffusion Models for Unsupervised Anomaly Detection in Brain Images.[[paper](https://arxiv.org/abs/2401.10561)]|arXiv, 20240119||||
|4|Mask, Stitch, and Re-Sample: Enhancing Robustness and Generalizability in Anomaly Detection through Automatic Diffusion Models.[[paper](https://arxiv.org/abs/2305.19643)]|arXiv, 20230531||||
|5|Lightening Anything in Medical Images.[[paper](https://arxiv.org/abs/2406.10236)][[code](https://github.com/Fayeben/UniMIE)]|arXiv, 20240601||||
|6|LighTDiff: Surgical Endoscopic Image Low-Light Enhancement with T-Diffusion.[[paper](https://arxiv.org/abs/2405.10550)][[code](https://github.com/DavisMeee/LighTDiff)]|MICCAI, 20240517||||
|7|Towards Learning Contrast Kinetics with Multi-Condition Latent Diffusion Models.[[paper](https://arxiv.org/abs/2403.13890)][[code](https://github.com/RichardObi/ccnet)]|arXiv, 20240320||||
|8|Step-Calibrated Diffusion for Biomedical Optical Image Restoration.[[paper](https://arxiv.org/abs/2403.13680)][[code](https://github.com/MLNeurosurg/restorative_step-calibrated_diffusion)]|arXiv, 20240320||||
|9|LLCaps: Learning to Illuminate Low-Light Capsule Endoscopy with Curved Wavelet Attention and Reverse Diffusion.[[paper](https://arxiv.org/abs/2307.02452)][[code](https://github.com/longbai1006/LLCaps)]|arXiv, 20230705||||
|10|Efficient Medicinal Image Transmission and Resolution Enhancement via GAN.[[paper](https://doi.org/10.48550/arXiv.2411.12833)]|arXiv,20241119||||



## 6 image reconstruction
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|Application of generative adversarial networks in image, face reconstruction and medical imaging: challenges and the current progress.[[paper](https://doi.org/10.1080/21681163.2024.2330524)]|||||
|2|HF-ResDiff: High-Frequency-Guided Residual Diffusion for Multi-dose PET Reconstruction.[[paper](https://doi.org/10.1007/978-3-031-72104-5_36)][[code]()]|Springer,20241003||||
|3|DiffCMR Fast Cardiac MRI Reconstruction with Diffusion Probabilistic Models.[[paper](https://doi.org/10.48550/arXiv.2312.04853)]|||||
|4|.[[paper]()][[code]()]|||||
|5|.[[paper]()][[code]()]|||||
|6|.[[paper]()][[code]()]|||||
|7|.[[paper]()][[code]()]|||||
|8|.[[paper]()][[code]()]|||||
|9|.[[paper]()][[code]()]|||||
|10|.[[paper]()][[code]()]|||||

## 7 image augmentation
|No.| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|---------|
|1|orGAN: A Synthetic Data Augmentation Pipeline for Simultaneous Generation of Surgical Images and Ground Truth Labels.[[paper](https://arxiv.org/abs/2506.14303)]|arXiv,20250617||||
|2|.[[paper]()][[code]()]|||||
|3|.[[paper]()][[code]()]|||||
|4|.[[paper]()][[code]()]|||||
|5|.[[paper]()][[code]()]|||||
|6|.[[paper]()][[code]()]|||||
|7|.[[paper]()][[code]()]|||||
|8|.[[paper]()][[code]()]|||||
|9|.[[paper]()][[code]()]|||||
|10|.[[paper]()][[code]()]|||||

# Dataset process and structure
## MR
### Brain
```markdown
Brain_MR_train_val_test
├── train
│   ├── TCGA-02-0006
│   │   ├── TCGA-02-0006_1996.08.23_t1.nii.gz
│   │   ├── TCGA-02-0006_1996.08.23_t1Gd.nii.gz
│   │   ├── TCGA-02-0006_1996.08.23_t2.nii.gz
│   │   ├── TCGA-02-0006_1996.08.23_flair.nii.gz
│   │   ├── TCGA-02-0006_1996.08.23_GlistrBoost.nii.gz   （mask）
│   │   ├── TCGA-02-0006_1996.08.23_GlistrBoost_ManuallyCorrected.nii.gz （人工矫正过的mask，不是每一个都有）
│   └── ...
├── val
│   ├── TCGA-08-0350
│   │   ├── TCGA-08-0350_1998.12.15_t1.nii.gz
│   │   ├── TCGA-08-0350_1998.12.15_t1Gd.nii.gz
│   │   ├── TCGA-08-0350_1998.12.15_t2.nii.gz
│   │   ├── TCGA-08-0350_1998.12.15_flair.nii.gz
│   │   ├── TCGA-08-0350_1998.12.15__GlistrBoost.nii.gz
│   │   ├── TCGA-08-0350_1998.12.15_GlistrBoost_ManuallyCorrected.nii.gz
│   └── ...
├── test
│   ├── TCGA-02-0003
│   │   ├── TCGA-02-0003_1997.06.08_t1.nii.gz
│   │   ├── TCGA-02-0003_1997.06.08_t1Gd.nii.gz
│   │   ├── TCGA-02-0003_1997.06.08_t2.nii.gz
│   │   ├── TCGA-02-0003_1997.06.08_flair.nii.gz
│   │   ├── TCGA-02-0003_1997.06.08_GlistrBoost.nii.gz
│   │   ├── TCGA-02-0003_1997.06.08_GlistrBoost_ManuallyCorrected.nii.gz
│   └── ...
└── survival_evaluation.csv
处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码（不同病例就不分文件夹了，直接都放一起，用前缀区分病例，后缀区分slice）
├── T1_T1CE
│   ├── train
│   │   ├── TCGA-02-0006_0.png
│   │   ├── TCGA-02-0006_1.png
│   │   ├── ...
│   ├── val
│   │   ├── TCGA-08-0350_0.png
│   │   ├── TCGA-08-0350_1.png 
│   │   ├── ...
│   ├── test
│   │   ├── TCGA-02-0003_0.png
│   │   ├── TCGA-02-0003_1.png
│   │   ├── ...
```
### Breast
```markdown
包含三个公开乳腺癌数据集，已经按照比例做了合并（.mat格式版本）--> 后面会数据处理成nii版本
Breast_MR_train_val_test
├── train
│   │   ├── ISPY1_1001.mat
│   │   ├── ...
│   │   ├── UCSF-BR-01.mat
│   │   ├── ...
│   │   ├── TCGA-AO-A03M.mat
│   └── ...
├── val
│   │   ├── ISPY1_1001.mat
│   │   ├── ...
│   │   ├── UCSF-BR-01.mat
│   │   ├── ...
│   │   ├── TCGA-AO-A03M.mat
│   └── ...
├── test
│   │   ├── ISPY1_1001.mat
│   │   ├── ...
│   │   ├── UCSF-BR-01.mat
│   │   ├── ...
│   │   ├── TCGA-AO-A03M.mat
│   └── ...
└── survival_evaluation.csv
nii版本，待处理
breast_train_val_test
├── train
│   │   ├── 
│   │   ├── ...
│   │   ├── 
│   │   ├── ...
│   │   ├── 
│   └── ...
├── val
│   │   ├── 
│   │   ├── ...
│   │   ├── 
│   │   ├── ...
│   │   ├── 
│   └── ...
├── test
│   │   ├── 
│   │   ├── ...
│   │   ├── 
│   │   ├── ...
│   │   ├── 
│   └── ...
└── survival_evaluation.csv
处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码
BRATS17
├── T1_T1CE
│   ├── test
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── train
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── val
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
```
## CT
### Uterus Ovary
```markdown
Uterus_Ovary_CT_train_val_test
├── train
│   ├── C3N-00866
│   │   ├── 03-05-2000-NA-CT UROGRAPHY CT ABDOME-51999
│   │   │   ├── C3N-00866_2000-03-05_CT.nii
│   │   │   ├── C3N-00866_2000-03-05_CTC.nii
│   │   ├── 03-06-2001-NA-CT RENAL MASS-CT ABDOM-36960
│   │   │   ├── C3N-00866_2001-03-06_CT.nii
│   │   │   ├── C3N-00866_2001-03-06_CTC.nii
│   ├── TCGA-09-2055
│   │   ├── 04-09-1998-NA-CT Abdo UnEn-38384
│   │   │   ├── TCGA-09-2055_1998-04-09_CT.nii
│   │   │   ├── TCGA-09-2055_1998-04-09_CTC.nii
│   └── ...
└── val
│   ├── TCGA-25-2404
│   │   ├── 10-24-1986-NA-Abdomen01AbdPelvisRoutine Adult-19915
│   │   │   ├── TCGA-25-2404_1986-10-24_CT.nii
│   │   │   ├── TCGA-25-2404_1986-10-24_CTC.nii
│   └── ...
└── test
│   ├── TCGA-61-2003
│   │   ├── 01-26-1998-NA-CT ABDOMEN WITH AND WI-80554
│   │   │   ├── TCGA-61-2003_1998-01-26_CT.nii
│   │   │   ├── TCGA-61-2003_1998-01-26_CTC.nii
│   └── ...
└── survival_evaluation.csv
处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码
├── T1_T1CE
│   ├── train
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── val
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── test
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
```
### Adrenal
```markdown
Adrenal_CT_train_val_test
├── train
│   ├── Adrenal_Ki67_Seg_001
│   │   ├── 08-22-2000-NA-CT ABDOMEN-56266
│   │   │   ├── Adrenal_Ki67_Seg_001_2000-08-22_CT.nii
│   │   │   ├── Adrenal_Ki67_Seg_001_2000-08-22_CTC.nii
│   └── ...
└── val
│   ├── Adrenal_Ki67_Seg_037
│   │   ├── 02-09-2009-NA-CT Abdomen  Pelvis-63206
│   │   │   ├── Adrenal_Ki67_Seg_037_2009-02-09_CT.nii
│   │   │   ├── Adrenal_Ki67_Seg_037_2009-02-09_CTC.nii
│   └── ...
└── test
│   ├── Adrenal_Ki67_Seg_042
│   │   ├── 06-19-2011-NA-CT CHEST ABDOMEN PELVIS W WO CONTRAST-34088
│   │   │   ├── Adrenal_Ki67_Seg_042_2011-06-19_CT.nii
│   │   │   ├── Adrenal_Ki67_Seg_042_2011-06-19_CTC.nii
│   └── ...
└── survival_evaluation.csv
处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码
├── T1_T1CE
│   ├── train
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── val
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── test
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
```
### Bladder Kidney
```markdown
Bladder_Kidney_CT_train_val_test
├── train
│   ├── C3L-00815
│   │   ├── 12-14-2008-NA-CT ABDOMEN AND PELVIS-75669
│   │   │   ├── C3L-00815_2008-12-14_CT.nii
│   │   │   ├── C3L-00815_2008-12-14_CTC.nii
│   ├── KiTS-00000
│   │   ├── 06-29-2003-NA-threephaseabdomen-41748
│   │   │   ├── KiTS-00000_2003-06-29_CT.nii
│   │   │   ├── KiTS-00000_2003-06-29_CTC.nii
│   └── ...
└── val
│   ├── TCGA-CJ-5678
│   │   ├── 10-09-1993-NA-CT CAP-92267
│   │   │   ├── TCGA-CJ-5678_1993-10-09_CT.nii
│   │   │   ├── TCGA-CJ-5678_1993-10-09_CTC.nii
│   └── ...
└── test
│   ├── C3N-02263
│   │   ├── 10-06-2000-NA-AbdomenJamaBrzuszna3FazyOpoznione Adult-40401
│   │   │   ├── C3N-02263_2000-10-06_CT.nii
│   │   │   ├── C3N-02263_2000-10-06_CTC.nii
│   └── ...
└── survival_evaluation.csv
处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码
├── T1_T1CE
│   ├── train
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── val
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── test
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
```
### Lung
```markdown
Lung_CT_train_val_test
├── train
│   ├── CMB-LCA-MSB-00939
│   │   ├── 02-20-1960-NA-CTCAP-17196
│   │   │   ├── CMB-LCA-MSB-00939_1960-02-20_CT.nii
│   │   │   ├── CMB-LCA-MSB-00939_1960-02-20_CTC.nii
│   │   ├── ...
│   │   │   ├── ...
│   │   │   ├── ...
│   ├── C3L-01000
│   │   ├── 06-09-2011-NA-MSKT organov grudnoy k-18628
│   │   │   ├── C3L-01000_2011-06-09_CT.nii
│   │   │   ├── C3L-01000_2011-06-09_CTC.nii
│   └── ...
└── val
│   ├── PD-1-Lung-00011
│   │   ├── 06-18-2007-NA-CAP W CONTRAST-89422
│   │   │   ├── PD-1-Lung-00011_2007-06-18_CT.nii
│   │   │   ├── PD-1-Lung-00011_2007-06-18_CTC.nii
│   └── ...
└── test
│   ├── Lung_Dx-A0104
│   │   ├── 04-23-2011-NA-ch.3d ao.cta-41811
│   │   │   ├── Lung_Dx-A0104_2011-04-23_CT.nii
│   │   │   ├── Lung_Dx-A0104_2011-04-23_CTC.nii
│   └── ...
└── survival_evaluation.csv
处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码
├── T1_T1CE
│   ├── train
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── val
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── test
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
```
### Stomach Colon Liver Pancreas
```markdown
Stomach_Colon_Liver_Pancreas_CT_train_val_test
├── train
│   ├── C3L-00625
│   │   ├── 09-28-2003-NA-CT ABDOMEN NONENH  ENHANCEDAB-70477
│   │   │   ├── C3L-00625_2003-09-28_CT.nii
│   │   │   ├── C3L-00625_2003-09-28_CTC.nii
│   ├── HCC_001
│   │   ├── 04-21-2000-NA-CT ABDPEL WC-49771
│   │   │   ├── HCC_001_2000-04-21_CT.nii
│   │   │   ├── HCC_001_2000-04-21_CTC.nii
│   │   ├── 11-30-1999-NA-CT-CAP WWO CON-00377
│   │   │   ├── HCC_001_1999-11-30_CT.nii
│   │   │   ├── HCC_001_1999-11-30_CTC.nii
│   └── ...
└── val
│   ├── MSB-02169
│   │   ├── 03-26-1959-NA-CTCAP-75858
│   │   │   ├── MSB-02169_1959-03-26_CT.nii
│   │   │   ├── MSB-02169_1959-03-26_CTC.nii
│   └── ...
└── test
│   ├── TCGA-VQ-AA6J
│   │   ├── 05-30-2000-NA-AS-94537
│   │   │   ├── TCGA-VQ-AA6J_2000-05-30_CT.nii
│   │   │   ├── TCGA-VQ-AA6J_2000-05-30_CTC.nii
│   └── ...
└── survival_evaluation.csv
处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码
├── T1_T1CE
│   ├── train
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── val
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...
│   └── test
│   │   ├── .png 
│   │   ├── .png 
│   │   ├── ...



