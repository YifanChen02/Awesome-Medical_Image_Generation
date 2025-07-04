# Relation of 
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
## image synthesis
### GAN-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Synthetic PET from CT improves diagnosis and prognosis for lung cancer: Proof of concept.[[paper](https://www.sciencedirect.com/science/article/pii/S2666379124001071?via%3Dihub)][[code]()]|Cell Reports Medicine 24|||Lung|
|Image Synthesis in Multi-Contrast MRI With Conditional Generative Adversarial Networks.[[paper](https://ieeexplore.ieee.org/abstract/document/8653423)][[code](https://github.com/icon-lab/pGAN-cGAN)]|TMI 19|||Brain|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


### Transformer-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|ResViT: Residual vision transformers for multi-modal medical image synthesis.[[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9758823)][[code1](https://github.com/icon-lab/ResViT) [code2](https://github.com/CV-Reimplementation/ResViT-Reimplementation)]|TMI22|[[BrainMRI:IXI] [BraTS] [PelvisCT-MRI]|MRI(T1,T2,PD,FLAIR) & MRI->CT| Brain |
|One Model to Synthesize Them All: Multi-Contrast Multi-Scale Transformer for Missing Data Imputation.[[paper](https://arxiv.org/pdf/2204.13738)][[code]()]|TMI23|||Brain|
##  Diffusion-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|DDFM: Denoising Diffusion Model for Multi-Modality lmage Fusion.[[paper](https://arxiv.org/pdf/2303.06840)][[code](https://github.com/Zhaozixiang1228/MMIF-DDFM)]|ICCV23 Oral||||
| MedM2G: Unifying Medical Multi-Modal Generation via Cross-Guided Diffusion with Visual Invariant.[[paper](https://arxiv.org/abs/2403.04290)]| CVPR24 |[X-ray:[MIMIC-CXR](https://arxiv.org/abs/1901.07042)] [contextual medical images:[MedICat](https://github.com/allenai/medicat)] [[kaggle:MRI-CT](https://www.kaggle.com/datasets/chenghanpu/brain-tumor-mri-and-ct-scan)]|MRI<->MRI<->CT<->X-ray & text<->image<->image|Brain|
| CoLa-Diff: Conditional Latent Diffusion Model for Multi-Modal MRI Synthesis.[[paper](https://arxiv.org/abs/2303.14081)] | MICCAI23 |[[BraTS18]()] [[IXI]()]| MRI(T1,T1ce,T2,FLAIR) & MRI(T1,T2,PD) |Brain|
|Phy-Diff: Physics-guided Hourglass Diffusion Model for Diffusion MRI Synthesis⋆.[[paper](https://arxiv.org/abs/2406.03002)][[code]()]|MICCAI24|||Brain|
|Conditional Diffusion Models for Semantic 3D Brain MRI Synthesis.[[paper](https://arxiv.org/pdf/2305.18453)][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|Brain PET Synthesis from MRI Using Joint Probability Distribution of Diffusion Model at Ultrahigh Fields.[[paper](https://arxiv.org/pdf/2211.08901)][[code]()]|||||
|Bi-parametric prostate MR image synthesis using pathology and sequence-conditioned stable diffusion.[[paper](https://arxiv.org/pdf/2303.02094)][[code]()]|||||
|Cascaded Latent Diffusion Models for High-Resolution Chest X-ray Synthesis.[[paper](https://arxiv.org/pdf/2303.11224)][[code]()]|||||
|DDMM-Synth: A Denoising Diffusion Model for Cross-modal Medical Image Synthesis with Sparse-view Measurement Embedding.[[paper]()][[code]()]|||||
|Cycle-guided Denoising Diffusion Probability Model for 3D Cross-modality MRI Synthesis.[[paper](https://arxiv.org/pdf/2305.00042)][[code]()]|||||
|Make-A-Volume: Leveraging Latent Diffusion Models for Cross-Modality 3D Brain MRI Synthesis.[[paper](https://arxiv.org/pdf/2307.10094)][[code]()]|||||

###diffusion-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Brain PET Synthesis from MRI Using Joint Probability Distribution of Diffusion Model at Ultrahigh Fields.[[paper](https://arxiv.org/abs/2211.08901)][[code]()]|arXiv, 2022||||

### Mamba-based
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

##image-generation
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Fast-DDPM: Fast Denoising Diffusion Probabilistic Models for Medical Image-to-Image Generation.[[paper](https://arxiv.org/abs/2405.14802)][[code](https://github.com/mirthAI/Fast-DDPM)]|||||

##Image-Translation
### gan-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|CycleGAN:Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks.[[paper](https://arxiv.org/pdf/1703.10593)][[code](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/README.md)]|||||
|PIX2PIX:Image-to-Image Translation with Conditional Adversarial Networks.[[paper](https://arxiv.org/pdf/1611.07004)][[code](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/README.md)]|||||

### diffusion-based
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


##mamba-diffusion
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Soft Masked Mamba Diffusion Model for CT to MRI Conversion.[[paper](https://arxiv.org/abs/2406.15910)][[code](https://github.com/wongzbb/DiffMa-Diffusion-Mamba)]|||||

3dMedical Diffusion
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Medical Diffusion: Denoising Diffusion Probabilistic Models for 3D Medical Image Generation.[[paper](https://arxiv.org/pdf/2211.03364)][[code](https://github.com/FirasGit/medicaldiffusion)]||||MR:Knee breast brain CT:thoracic|
|.[[paper]()][[code]()]|||||



#others_image_translation
|Mitigating analytical variability in fMRI results with style transfer.[[paper](https://arxiv.org/abs/2404.03703)][[code]()]|||||
|Class-Guided Image-to-Image Diffusion: Cell Painting from Brightfield Images with Class Labels.[[paper](https://arxiv.org/abs/2303.08863)][[code](https://github.com/crosszamirski/guided-I2I)]|arXiv, 2023||||
|Diffusion Models for Contrast Harmonization of Magnetic Resonance Images.[[paper](https://arxiv.org/abs/2303.08189)][[code]()]|MIDL, 2023||||
|Conversion Between CT and MRI Images Using Diffusion and Score-Matching Models.[[paper](https://arxiv.org/abs/2209.12104)][[code]()]|arXiv, 2022||||
|A Novel Unified Conditional Score-based Generative Framework for Multi-modal Medical Image Completion.[[paper](https://arxiv.org/abs/2207.03430)][[code]()]|arXiv, 2022||||



## image_restoration
inpainting
Super Resolution
denoising
Enhancement

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
