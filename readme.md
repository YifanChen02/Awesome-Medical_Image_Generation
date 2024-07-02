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
## GAN-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|Synthetic PET from CT improves diagnosis and prognosis for lung cancer: Proof of concept.[[paper](https://www.sciencedirect.com/science/article/pii/S2666379124001071?via%3Dihub)][[code]()]|Cell Reports Medicine 24|||Lung|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


## Transformer-based
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
|Phy-Diff: Physics-guided Hourglass Diffusion Model for Diffusion MRI Synthesis⋆.[[paper](https://arxiv.org/abs/2406.03002)][[code]()]||||Brain|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||

## Mamba-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
| I2I-Mamba: Multi-modal medical image synthesis via selective state space modeling.[[paper](https://arxiv.org/abs/2405.14022)][[code](https://github.com/icon-lab/I2I-Mamba)]| |[[BrainMRI:IXI](https://brain-development.org/ixi-dataset/)] [[PelvisCT-MRI](https://zenodo.org/records/583096)]| MRI(T1,T2,PD) & MRI(T2w)->CT|Brain & Pelvis|
|VM-DDPM: Vision Mamba Diffusion for Medical Image Synthesis.[[paper]()][[code]()]|||||
|DiM: Diffusion Mamba for Efficient High-Resolution Image Synthesis.[[paper](https://arxiv.org/pdf/2405.14224)][[code](https://github.com/tyshiwo1/DiM-DiffusionMamba/)]||||High-Resolution Image Synthesis|

|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||


github:
图像生成(Image Generation/Image Synthesis) CVPR24 https://github.com/Kobaayyy/Awesome-CVPR2024-AIGC

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
