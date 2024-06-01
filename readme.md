# Paper & Code & Dataset
## GAN-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||
|.[[paper]()][[code]()]|||||

## Transformer-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|
|ResViT: Residual vision transformers for multi-modal medical image synthesis.[[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9758823)][[code1](https://github.com/icon-lab/ResViT) [code2](https://github.com/CV-Reimplementation/ResViT-Reimplementation)]|TMI22|[[BrainMRI:IXI] [BraTS] [PelvisCT-MRI]|MRI(T1,T2,PD,FLAIR) & MRI->CT| Brain |

##  Diffusion-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|

| MedM2G: Unifying Medical Multi-Modal Generation via Cross-Guided Diffusion with Visual Invariant.[[paper](https://arxiv.org/abs/2403.04290)][[code]()]| CVPR24 |[X-ray:[MIMIC-CXR](https://arxiv.org/abs/1901.07042)] [contextual medical images:[MedICat](https://github.com/allenai/medicat)] [[kaggle:MRI-CT](https://www.kaggle.com/datasets/chenghanpu/brain-tumor-mri-and-ct-scan)]|MRI<->MRI<->CT<->X-ray & text<->image<->image|Brain|
| CoLa-Diff: Conditional Latent Diffusion Model for Multi-Modal MRI Synthesis.[[paper](https://arxiv.org/abs/2303.14081)][[code]()] | MICCAI23 |[[BraTS18]()] [[IXI]()]| MRI(T1,T1ce,T2,FLAIR) & MRI(T1,T2,PD) |Brain|

## Mamba-based
| paper | 会议/期刊 | dataset | 分类 | 器官 |
|---------|---------|---------|---------|---------|

| I2I-Mamba: Multi-modal medical image synthesis via selective state space modeling.[[paper](https://arxiv.org/abs/2405.14022)][[code](https://github.com/icon-lab/I2I-Mamba)]| |[[BrainMRI:IXI](https://brain-development.org/ixi-dataset/)] [[PelvisCT-MRI](https://zenodo.org/records/583096)]| MRI(T1,T2,PD) & MRI(T2w)->CT|Brain & Pelvis|
|VM-DDPM: Vision Mamba Diffusion for Medical Image Synthesis.[[paper]()][[code]()]|||||
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
