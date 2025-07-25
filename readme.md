# 

# Updates

# Contents

## Image Generation Taxonomy
![Alt text](https://github.com/YifanChen-thu/Medical_Multi-Modal_Generation/blob/main/Mechanism_Architecture_page-0001.jpg)
![Alt text](https://github.com/YifanChen-thu/Medical_Multi-Modal_Generation/blob/main/ImageGeneration_page-0001.jpg)

# 
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
```markdown
```

# Paper & Code & Dataset
## 0 survey
### 0.1 all
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|The generative era of medical AI.[[paper](https://www.cell.com/cell/fulltext/S0092-8674(25)00568-9)][[code]()]|cell 2025||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 0.2 gan-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 0.3 transformer-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 0.4 diffusion-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Foundation Models for Music: A Survey.[[paper](https://arxiv.org/abs/2408.14340)][[code](https://github.com/nicolaus625/FM4Music)]|arXiv, 2024||||
|A Comprehensive Survey on Diffusion Models and Their Applications.[[paper](https://arxiv.org/abs/2408.10207)][[code]()]|arXiv, 2024||||
|Physics-Inspired Generative Models in Medical Imaging: A Review.[[paper]()][[code]()]|https://arxiv.org/abs/2407.10856|arXiv, 2024|||
|Artifact Reduction in 3D and 4D Cone-beam Computed Tomography Images with Deep Learning -- A Review.[[paper](https://arxiv.org/abs/2403.18565)][[code]()]|arXiv, 2024||||
|A Survey of Emerging Applications of Diffusion Probabilistic Models in MRI.[[paper](https://arxiv.org/abs/2311.11383)][[code]()]|arXiv, 2023||||
|A Comprehensive Review of Generative AI in Healthcare.[[paper](https://arxiv.org/abs/2310.00795)][[code]()]|arXiv, 2023||||
|Generative AI for Medical Imaging: extending the MONAI Framework.[[paper](https://arxiv.org/abs/2307.15208)][[code](https://github.com/Project-MONAI/GenerativeModels)]|||||
|Deep Learning Approaches for Data Augmentation in Medical Imaging: A Review.[[paper](https://arxiv.org/abs/2307.13125)][[code]()]|Journal of Imaging, 2023|arXiv, 2023|||
|A Comprehensive Survey on Generative Diffusion Models for Structured Data.[[paper](https://arxiv.org/abs/2306.04139)][[code]()]|arXiv, 2023||||
|Diffusion Models in Medical Imaging: A Comprehensive Survey.[[paper](https://arxiv.org/abs/2211.07804)][[code]()]|MedIA Journal, 2023||||
|Efficient Diffusion Models for Vision: A Survey.[[paper](https://arxiv.org/abs/2210.09292)][[code]()]|arXiv, 2022||||
|Diffusion Models in Vision: A Survey.[[paper](https://arxiv.org/pdf/2209.04747.pdf)][[code](https://github.com/CroitoruAlin/Diffusion-Models-in-Vision-A-Survey)]|arXiv, 2022||||
|A Survey on Generative Diffusion Model.[[paper](https://arxiv.org/pdf/2209.02646.pdf)][[code](https://github.com/chq1155/A-Survey-on-Generative-Diffusion-Model)]|arXiv, 2022||||
|Diffusion Models: A Comprehensive Survey of Methods and Applications.[[paper](https://arxiv.org/pdf/2209.00796)][[code](https://github.com/YangLing0818/Diffusion-Models-Papers-Survey-Taxonomy)]|arXiv, 2022||||
|A Survey on Graph Diffusion Models: Generative AI in Science for Molecule, Protein and Material.[[paper](https://arxiv.org/abs/2304.01565)][[code]()]|arXiv, 2023||||
|Diffusion Models in Low-Level Vision: A Survey.[[paper](https://arxiv.org/abs/2406.11138)][[code](https://github.com/ChunmingHe/awesome-diffusion-models-in-low-level-vision)]|arXiv, 2024||||
|Diffusion Models for Time Series Applications: A Survey.[[paper](https://arxiv.org/abs/2305.00624)][[code]()]|arXiv, 2023||||
|A Comprehensive Survey on Knowledge Distillation of Diffusion Models.[[paper](https://arxiv.org/abs/2304.04262)][[code]()]|arXiv, 2023||||

### 0.5 mamba-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 0.6 flow-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 0.7 rnn-based(rwkv)
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


## 1 Image synthesis
### 1.1 GAN-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Synthetic PET from CT improves diagnosis and prognosis for lung cancer: Proof of concept.[[paper](https://www.sciencedirect.com/science/article/pii/S2666379124001071?via%3Dihub)][[code]()]|Cell Reports Medicine 24|||Lung|
|Image Synthesis in Multi-Contrast MRI With Conditional Generative Adversarial Networks.[[paper](https://ieeexplore.ieee.org/abstract/document/8653423)][[code](https://github.com/icon-lab/pGAN-cGAN)]|TMI 19|||Brain|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


### 1.2 Transformer-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|ResViT: Residual vision transformers for multi-modal medical image synthesis.[[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9758823)][[code1](https://github.com/icon-lab/ResViT) [code2](https://github.com/CV-Reimplementation/ResViT-Reimplementation)]|TMI22|[[BrainMRI:IXI] [BraTS] [PelvisCT-MRI]|MRI(T1,T2,PD,FLAIR) & MRI->CT| Brain |
|One Model to Synthesize Them All: Multi-Contrast Multi-Scale Transformer for Missing Data Imputation.[[paper](https://arxiv.org/pdf/2204.13738)][[code]()]|TMI23|||Brain|


### 1.3 Diffusion-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
| MedM2G: Unifying Medical Multi-Modal Generation via Cross-Guided Diffusion with Visual Invariant.[[paper](https://arxiv.org/abs/2403.04290)]| CVPR24 |[X-ray:[MIMIC-CXR](https://arxiv.org/abs/1901.07042)] [contextual medical images:[MedICat](https://github.com/allenai/medicat)] [[kaggle:MRI-CT](https://www.kaggle.com/datasets/chenghanpu/brain-tumor-mri-and-ct-scan)]|MRI<->MRI<->CT<->X-ray & text<->image<->image|Brain|
| CoLa-Diff: Conditional Latent Diffusion Model for Multi-Modal MRI Synthesis.[[paper](https://arxiv.org/abs/2303.14081)] | MICCAI23 |[[BraTS18]()] [[IXI]()]| MRI(T1,T1ce,T2,FLAIR) & MRI(T1,T2,PD) |Brain|
|Phy-Diff: Physics-guided Hourglass Diffusion Model for Diffusion MRI Synthesis⋆.[[paper](https://arxiv.org/abs/2406.03002)][[code]()]|MICCAI24|||Brain|
|Conditional Diffusion Models for Semantic 3D Brain MRI Synthesis.[[paper](https://arxiv.org/pdf/2305.18453)][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|Brain PET Synthesis from MRI Using Joint Probability Distribution of Diffusion Model at Ultrahigh Fields.[[paper](https://arxiv.org/abs/2211.08901)][[code]()]|arXiv, 2022||||
|Bi-parametric prostate MR image synthesis using pathology and sequence-conditioned stable diffusion.[[paper](https://arxiv.org/pdf/2303.02094)][[code]()]|||||
|Cascaded Latent Diffusion Models for High-Resolution Chest X-ray Synthesis.[[paper](https://arxiv.org/pdf/2303.11224)][[code]()]|||||
|DDMM-Synth: A Denoising Diffusion Model for Cross-modal Medical Image Synthesis with Sparse-view Measurement Embedding.[[paper]()][[code]()]|||||
|Cycle-guided Denoising Diffusion Probability Model for 3D Cross-modality MRI Synthesis.[[paper](https://arxiv.org/pdf/2305.00042)][[code]()]|||||
|Make-A-Volume: Leveraging Latent Diffusion Models for Cross-Modality 3D Brain MRI Synthesis.[[paper](https://arxiv.org/pdf/2307.10094)][[code]()]|||||


### 1.4 Mamba-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
| I2I-Mamba: Multi-modal medical image synthesis via selective state space modeling.[[paper](https://arxiv.org/abs/2405.14022)][[code](https://github.com/icon-lab/I2I-Mamba)]| |[[BrainMRI:IXI](https://brain-development.org/ixi-dataset/)] [[PelvisCT-MRI](https://zenodo.org/records/583096)]| MRI(T1,T2,PD) & MRI(T2w)->CT|Brain & Pelvis|
|VM-DDPM: Vision Mamba Diffusion for Medical Image Synthesis.[[paper](https://arxiv.org/abs/2405.05667)][[code]()]|||||
|DiM: Diffusion Mamba for Efficient High-Resolution Image Synthesis.[[paper](https://arxiv.org/pdf/2405.14224)][[code](https://github.com/tyshiwo1/DiM-DiffusionMamba/)]||||High-Resolution Image Synthesis|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


github:
图像生成(Image Generation/Image Synthesis) CVPR24 https://github.com/Kobaayyy/Awesome-CVPR2024-AIGC



## 2 Image-Translation
### 2.1 gan-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|CycleGAN:Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks.[[paper](https://arxiv.org/pdf/1703.10593)][[code](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/README.md)]|||||
|PIX2PIX:Image-to-Image Translation with Conditional Adversarial Networks.[[paper](https://arxiv.org/pdf/1611.07004)][[code](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/README.md)]|||||

### 2.2 diffusion-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Cross-conditioned Diffusion Model for Medical Image to Image Translation.[[paper](https://arxiv.org/abs/2409.08500)][[code]()]|MICCAI, 2024||||
|Slice-Consistent 3D Volumetric Brain CT-to-MRI Translation with 2D Brownian Bridge Diffusion Model.[[paper](https://arxiv.org/abs/2407.05059)][[code](https://github.com/MICV-yonsei/CT2MRI)]|MICCAI, 2024||||
|2.5D Multi-view Averaging Diffusion Model for 3D Medical Image Translation: Application to Low-count PET Reconstruction with CT-less Attenuation Correction.[[paper](https://arxiv.org/abs/2406.08374)][[code]()]|||||
|Similarity-aware Syncretic Latent Diffusion Model for Medical Image Translation with Representation Learning.[[paper](https://arxiv.org/abs/2406.13977)][[code]()]|||||
|Cascaded Multi-path Shortcut Diffusion Model for Medical Image Translation.[[paper](https://arxiv.org/abs/2405.12223)][[code]()]|||||
|Diffusion based Zero-shot Medical Image-to-Image Translation for Cross Modality Segmentation.[[paper](https://arxiv.org/abs/2404.01102)][[code]()]|||||
|Self-Consistent Recursive Diffusion Bridge for Medical Image Translation.[[paper](https://arxiv.org/abs/2405.06789)][[code](https://github.com/icon-lab/SelfRDB)]|||||
|Tackling Structural Hallucination in Image Translation with Local Diffusion.[[paper](https://arxiv.org/abs/2404.05980)][[code]()]|||||
|ContourDiff: Unpaired Image Translation with Contour-Guided Diffusion Models.[[paper](https://arxiv.org/abs/2403.10786)][[code]()]|||||
|FDDM: Unsupervised Medical Image Translation with a Frequency-Decoupled Diffusion Model.[[paper](https://arxiv.org/abs/2311.12070)][[code]()]|||||
|Adaptive Latent Diffusion Model for 3D Medical Image to Image Translation: Multi-modal Magnetic Resonance Imaging Study.[[paper](https://arxiv.org/abs/2311.00265)][[code](https://github.com/jongdory/ALDM/)]|WACV, 2024||||
|Cycle-guided Denoising Diffusion Probability Model for 3D Cross-modality MRI Synthesis.[[paper](https://arxiv.org/abs/2305.00042)][[code]()]|arXiv, 2023||||
|Zero-shot Medical Image Translation via Frequency-Guided Diffusion Models.[[paper](https://arxiv.org/abs/2304.02742)][[code](https://github.com/Kent0n-Li/FGDM)]|arXiv, 2023||||
|Zero-shot-Learning Cross-Modality Data Translation Through Mutual Information Guided Stochastic Diffusion.[[paper](https://arxiv.org/abs/2301.13743)][[code]()]|arXiv, 2023||||
|Unsupervised Medical Image Translation with Adversarial Diffusion Models.[[paper](https://arxiv.org/abs/2207.08208)][[code]()]|IEEE TMI Journal, 2022||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


### mamba-diffusion
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Soft Masked Mamba Diffusion Model for CT to MRI Conversion.[[paper](https://arxiv.org/abs/2406.15910)][[code](https://github.com/wongzbb/DiffMa-Diffusion-Mamba)]|||||





## others_image_translation
|Mitigating analytical variability in fMRI results with style transfer.[[paper](https://arxiv.org/abs/2404.03703)][[code]()]|||||
|Class-Guided Image-to-Image Diffusion: Cell Painting from Brightfield Images with Class Labels.[[paper](https://arxiv.org/abs/2303.08863)][[code](https://github.com/crosszamirski/guided-I2I)]|arXiv, 2023||||
|Diffusion Models for Contrast Harmonization of Magnetic Resonance Images.[[paper](https://arxiv.org/abs/2303.08189)][[code]()]|MIDL, 2023||||
|Conversion Between CT and MRI Images Using Diffusion and Score-Matching Models.[[paper](https://arxiv.org/abs/2209.12104)][[code]()]|arXiv, 2022||||
|A Novel Unified Conditional Score-based Generative Framework for Multi-modal Medical Image Completion.[[paper](https://arxiv.org/abs/2207.03430)][[code]()]|arXiv, 2022||||

## 3. image_fusion
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|DDFM: Denoising Diffusion Model for Multi-Modality Image Fusion.[[paper](https://arxiv.org/pdf/2303.06840)][[code](https://github.com/Zhaozixiang1228/MMIF-DDFM)]|ICCV23 Oral||||
|Medical image fusion: A survey of the state of the art.[[paper](https://pdf.sciencedirectassets.com/272144/1-s2.0-S1566253514X00023/1-s2.0-S1566253513001450/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEPb%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJGMEQCIFSblswro6NOny2eHY8wOIdFCs8zr6ArK9dIRGHj9Zp7AiAQ9T%2FJG6g5Vwao9fTkSQ7eWnWJnh6J005Jgz40mbPR%2BSqzBQgfEAUaDDA1OTAwMzU0Njg2NSIMXRoLwZjNoBgEzBpcKpAFPwzhPcR6FbtWMIUsKGQdXFuPPkzUd2odEoz%2BwGMSUL4P%2FPrGdV7h5Qn6ojyGVR5j7MR6zNjUpQTiyb9J%2F5doKQB%2FOKS%2F1LhKHvlRKeiZGtMInnuLyfrAZqBkOxFohbhP10mk8OjjIs%2F67GMw%2BamEkAbHBQacdNy14d5MrvBCxRKUMfZHpQVto7hW8sFrlsSEDkuc1pnBzoVxw7bIdX5uYgKZ965uPUvKXqXx1rnSg6A1%2FOGwC1n9C7Aco33th%2BkZo68Xg0pTf57NBvzVxtu81UY8J6prbgpB5pGtY66OvPyc7DqBRSs8XBvRnhnp3QNeln9XZnBZgiCsAbwSJleWcGof5gx1i2YUmWPu5U00yn%2BGo%2BmVb4ZwCxX2q3%2BeOo3z6in6F3vPtXWIYujwPO8TvovtPCdT8Hsd1W0iuOhnzUdKU0SdjKlvLSpOKNBzdeXGLDKF8Bjls6B301mgbvIVdeuRvkHZGftwAsKSyX6tEEaN0RtrfrtJWbUEek%2Bc8S6NWXZVUB4ZRQGl1L2r6wgajUVfznFu%2BBeUKVbLkLKiSO%2BbwCmwOI3wsh%2BmUb%2FgFMAgUACdXKw4H7ZU4tU1YBQlFQIDxm7fs75kyRLR%2F0zbSKCXZVk1yTJnuauOJX0WNHzR4dSqtSCqKTASqvAqXDsnDQGj027%2F4yMuDplK5nDEA6uEagroWNkSVZ6QOPBRnwpA6YF7f6S%2B9cFUNPUUXnirFXq%2FjfRIO553XL7xRxMpv7%2FztWmr%2Fs%2Feqksz%2BcACHowG3CRbi3RwgPg1nlYt45pqaMX%2Bc5AsDOZ1FTlh5XGJWnVpk5389xvjvdzanakWuthChpdy9DH7qgwoRD7cj9IH8CjNXdj2eScEDf%2FkQaeUA30whq2FxAY6sgH6vmWnN9tlG5IAdiv0thO5l%2BThdoTaiRgMqm%2F1wSvdgWI%2FsM1OJYU%2BzY9%2FmdcrliUZlguieimDu9oVFJeGqRyVXnT6XVctRGQqH41uasSe6z9BE8j5rs6GlMBvcYM8VNdnZvthcIhdh1It%2FZPGe9KybzK%2BlEgrrtBGrqYVl%2Fm9S%2B5h1HraG5Ht9N1SwETbqjL4YbzgdCRxMegun3FNTy8payFghEzubu3ls22InQbGqqOT&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20250723T220110Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYZMAMDVHK%2F20250723%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=b94cc9c2524e77d5ab5c88adc2fc34cd98f1a948493de04def05977a5714cbe2&hash=c597026fdf1d26e2ff05258d0c772738e6f9e382ee68d71374ef369a10f901ce&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S1566253513001450&tid=spdf-d86eebfb-624f-462a-a98b-473c0f0375b5&sid=6142a02e9278d94d80087fc936726e8b4fdcgxrqb&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&rh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=1d045b585c01575354&rr=963e7471fc290f12&cc=gb)][[code]()]|Information Fusion 2014||||
|Medical image fusion with deep neural networks.[[paper](https://www.nature.com/articles/s41598-024-58665-9)][[code]()]|Scientific Reports 2024||||
|LFDT-Fusion: A latent feature-guided diffusion Transformer model for general image fusion.[[paper](https://www.sciencedirect.com/science/article/pii/S1566253524004172)][[code]()]|Information Fusion 2025||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||

## 4. image-generation
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Medical Diffusion: Denoising Diffusion Probabilistic Models for 3D Medical Image Generation.[[paper](https://arxiv.org/pdf/2211.03364)][[code](https://github.com/FirasGit/medicaldiffusion)]||||MR:Knee breast brain CT:thoracic|
|Fast-DDPM: Fast Denoising Diffusion Probabilistic Models for Medical Image-to-Image Generation.[[paper](https://arxiv.org/abs/2405.14802)][[code](https://github.com/mirthAI/Fast-DDPM)]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||

## 5. image_restoration
### 5.0 restoration
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Restore-RWKV: Efficient and Effective Medical Image Restoration with RWKV.[[paper](https://arxiv.org/pdf/2407.11087)][[code](https://github.com/Yaziwel/Restore-RWKV)]|arxiv20250106||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||

### 5.1 inpainting
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 5.2 Super Resolution
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 5.3 denoising
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
### 5.4 Enhancement
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


# Dataset process and structure
## BRATS17
```markdown
BRATS17
├── Brats17TestingData
│   ├── Brats17_2013_31_1
│   │   ├── Brats17_2013_31_1_flair.nii
│   │   ├── Brats17_2013_31_1_t1.nii
│   │   ├── Brats17_2013_31_1_t1ce.nii
│   │   ├── Brats17_2013_31_1_t2.nii
│   └── ...
│   └── survival_evaluation.csv
└── Brats17TrainingData
│   ├── HGG
│   │   ├── Brats17_2013_3_1
│   │   │   ├── Brats17_2013_3_1_flair.nii
│   │   │   ├── Brats17_2013_3_1_seg.nii
│   │   │   ├── Brats17_2013_3_1_t1.nii
│   │   │   ├── Brats17_2013_3_1_t1ce.nii
│   │   │   ├── Brats17_2013_3_1_t2.nii
│   │   │   ├── ROI_Brats17_2013_3_1_t1.nii
│   │   ├── ...
│   └── LGG
│   │   ├── Brats17_2013_0_1
│   │   │   ├── Brats17_2013_0_1_flair.nii
│   │   │   ├── Brats17_2013_0_1_seg.nii
│   │   │   ├── Brats17_2013_0_1_t1.nii
│   │   │   ├── Brats17_2013_0_1_t1ce.nii
│   │   │   ├── Brats17_2013_0_1_t2.nii
│   │   │   ├── ROI_Brats17_2013_0_1_t1.nii
│   │   ├── ...
│   └── survival_data.csv
└── Brats17ValidationData
│   ├── Brats17_CBICA_AAM_1
│   │   ├── Brats17_CBICA_AAM_1_flair.nii
│   │   ├── Brats17_CBICA_AAM_1_t1.nii
│   │   ├── Brats17_CBICA_AAM_1_t1ce.nii
│   │   ├── Brats17_CBICA_AAM_1_t2.nii
│   └── ...
│   └── survival_evaluation.csv

处理之后(将t1和t1ce左右拼成一个新的图png)——有对应代码
BRATS17
├── T1_T1CE
│   ├── test
│   │   ├── Brats17_2013_31_1_0.png 
│   │   ├── Brats17_2013_31_1_1.png 
│   │   ├── ...
│   └── train
│   │   ├── Brats17_2013_3_1_0.png 
│   │   ├── Brats17_2013_3_1_1.png 
│   │   ├── ...
│   └── val
│   │   ├── Brats17_CBICA_AAM_1_0.png 
│   │   ├── Brats17_CBICA_AAM_1_1.png 
│   │   ├── ...
```
