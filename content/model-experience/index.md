---
title: "AI Model Experience"
summary: "Comprehensive record of deep learning architectures, foundation models, frameworks, and medical imaging tasks Winston (Weijie) Chen has worked with (~2018–present)."
date: 2025-07-01
type: landing

sections:
  - block: markdown
    content:
      title: AI Model Experience
      text: |
        Structured reference of every deep learning architecture, foundation model, framework, and clinical task I have hands-on experience with. Intended to be both human-readable and machine-parseable.

        ---

        ## CNN Architectures

        | Model | Task | Notes |
        |---|---|---|
        | **U-Net** (2D) | Image segmentation, synthesis | PET/MR translation; Yoshi → Magikarp → Zapdos → Chansey iterations |
        | **U-Net** (3D) | Volumetric segmentation | 3D MR segmentation for head & neck tumor |
        | **Pyramid CNN** | Longitudinal 3D segmentation | Spatial + temporal attention; 1st place MICCAI HNTS-MRG 2024 |
        | **CycleGAN** | Unpaired image translation | PET/MR synthesis; MIMRTL_cGAN, MIMRTL_2dCycleGAN |
        | **Conditional GAN (cGAN)** | Paired image translation | PET→CT, NAC→MAC; multiple iterations |
        | **Y-Net** | NAC PET correction | PSF + Gibbs artifact correction |
        | **FourierU-Net** | Image translation | Skip connection and backbone feature analysis |
        | **ResNet variants** | Feature extraction | Backbone in multiple pipelines |
        | **Encoder-Decoder (VQ)** | PET→CT synthesis | SharkSeagrass project |

        ---

        ## Transformer Architectures

        | Model | Task | Notes |
        |---|---|---|
        | **Vision Transformer (ViT)** | Classification, synthesis | BAE-ViT bone age; multimodal fusion |
        | **TransUNet** | Synthetic CT generation | CNN + Transformer hybrid; ISMRM 2022 comparison |
        | **SwinIR** | Synthetic CT generation | Swin Transformer; ISMRM 2022 comparison |
        | **UNETR** | NAC→CT translation | Transformer-based UNet for 3D medical images |
        | **Masked Autoencoder (MAE)** | Self-supervised pretraining | MedMAE — unified encoder for MR, PET, CT |
        | **Cross-modal Bi-Attention** | Multimodal fusion | CT + clinical text for MACE prediction (Mayo Clinic) |
        | **DuettoSyn** | PET/MR synthesis | Custom transformer-based image translation |

        ---

        ## Generative & Diffusion Models

        | Model | Task | Notes |
        |---|---|---|
        | **DDPM** (Diffusion) | Medical image translation | NAC PET → CTAC; diffusion101 implementation |
        | **Cold Diffusion** | Medical image synthesis | Adapted cold diffusion framework |
        | **Conditional Wavelet Diffusion (cWDM)** | Cross-modality 3D synthesis | BraTS 2024 adaptation |
        | **LakeLatios** | Paired image translation | Diffusion model exploration |

        ---

        ## Foundation Models Used

        | Model | Domain | Application |
        |---|---|---|
        | **MAISI** (NVIDIA) | Medical imaging | Synthetic CT from segmentation maps; NAC PET → CT pipeline |
        | **Vision–Language Models** (generic) | Multimodal | MACE prediction from CT + clinical text (Mayo Clinic) |
        | **TotalSegmentator / nnUNet** | Medical segmentation | easy_nnUNet; ALTS active learning extension |

        ---

        ## Federated Learning

        | Framework | Notes |
        |---|---|
        | **SASWISE-Fed** | Modular block design with weight obfuscation, adversarial monitoring, uncertainty estimation |
        | **FedFBD / MedMNIST_FBD** | Federated block design experiments on MedMNIST |

        ---

        ## Uncertainty Estimation

        | Method | Notes |
        |---|---|
        | **SASWISE-UE** | Scalable ensemble (CNN + ViT variants); R² = 0.98 seg / 0.80 syn; 93.75% efficiency gain |
        | **Variance across model sub-networks** | Real-time performance surveillance for clinical deployment |

        ---

        ## Medical Imaging Tasks

        | Task | Modalities | Key Projects |
        |---|---|---|
        | **Synthetic CT generation** | MRI → CT | SyntheticCT_Brain, ISMRM 2022, deepMRAC |
        | **Attenuation correction** | NAC PET → CTAC | NasCent, NAC2PET, DeepMRAC |
        | **Partial volume correction** | PET + MRI | Yoshi_PVC, MIMRTL_PVC, SNMMI 2020 |
        | **Tumor segmentation** | 3D MRI | HNTS-MRG 2024 (1st place), head & neck RT |
        | **Motion correction** | PET | 4D deformation fields, PET1503 cohort |
        | **Low-dose enhancement** | FDG PET/MR | Crohn's disease, deep learning reconstruction |
        | **Bone age estimation** | X-ray | BAE-ViT, multimodal ViT |
        | **Cardiovascular risk** | CT + EHR text | MACE prediction, opportunistic screening |
        | **Image registration** | PET/CT | Affine + deformable registration |
        | **Object detection** | RGB | Low-light detection (arXiv 2021) |

        ---

        ## Frameworks & Tools

        | Category | Tools |
        |---|---|
        | **Deep Learning** | PyTorch, TensorFlow, Keras, MONAI |
        | **Medical Imaging** | ITK-SNAP, SimpleITK, NiBabel, PETPVC |
        | **HPC / Scheduling** | Slurm, HTCondor (UW-CHTC), DGX GPU servers |
        | **Cloud** | Azure, AWS, Google Colab |
        | **DevOps** | Docker, Git, Anaconda, Linux |
        | **Languages** | Python, MATLAB, Julia, C, SQL, D3.js |
        | **Visualization** | Seaborn, Matplotlib, D3.js |

        ---

        ## Dataset Experience

        | Dataset | Modality | Task |
        |---|---|---|
        | MIMRTL in-house (~70 subjects) | Brain MRI | Synthetic CT |
        | PET1503 cohort (5 subjects) | PET | Motion correction |
        | deepMRAC cohort (~40 subjects) | Whole-body PET/MR | Attenuation correction |
        | Crohn's disease (20 subjects) | MRE | Low-dose PET/MR |
        | HNTS-MRG 2024 (150 patients) | 3D MRI | Longitudinal segmentation |
        | NEMA phantom | PET/CT | Synthesis validation |
        | TCIA Breast | CT | Segmentation |
        | MedMNIST | Multi-modal | Federated learning |
---
