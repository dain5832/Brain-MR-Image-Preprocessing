# Brain_MR_Image_Preprocessing
Preprocessing pipeline of Brain MR Image for medical research.

## Overview
![alt text](/readme_img/1_Overview.PNG)


## Tools
### 1)ANTs(Advanced Normalization Tools) 
- A tool for biomedical image analysis with a focus on registration, segmentation, etc. 
- Used for Resampling, N4 Bias Correction, Co-registration 

### MONSTR(Multi-cONtrast brain STRipping method ) 
- A software tool to generate brain masks (or skull-strip) from multi-contrast MR brain images, such as T1, T2, PD, or FLAIR. 
- Compared to other tools that are validated on T1-based skull stripping methods, MONSTR involves multi-modal inputs(T1, T2, FLAIR를 지원)와 multi-model atlases.
- Used for Skull Stripping

*For installation of preprocessing tools and code usage, check out reference.md.*

## Step
1) Resampling
- Resize voxel to 1X1X1.

2) N4 Bias Correction
- Method for correcting low frequency intensity non-uniformity present in MRI image data known as a bias or gain field.

3) Co-Registration (to T1C)
- Brings one image(mostly T1C) to match another image, such that the same voxels refers roughly to the same structure in both brains.

4) Skull-Stripping + Apply skull mask
- Generate skull mask for each brain image, and strip.
