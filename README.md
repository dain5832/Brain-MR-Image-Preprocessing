# Brain_MR_Image_Preprocessing
Preprocessing pipeline of Brain MR Image for medical research. 

**For installation of preprocessing tools and code usage, check out [reference.md](/reference.md).*

## Update log
**6/22** \
Code that applies brain mask added.

**6/23** \
New variable T1C_label added.

**7/6** \
New variable mask_label added.

**7/7** \
'try-except' was added when finding T1Cpath and T2path using glob since the files might not exist.

**8/4** \
Clean outputdir(MONSTR) before skull-stripping added.

## Overview
![alt text](/readme_img/1_Overview.PNG)


## Tools
### 1)[ANTs](https://github.com/ANTsX/ANTs)(Advanced Normalization Tools)
- A tool for biomedical image analysis with a focus on registration, segmentation, etc. 
- Used for Resampling, N4 Bias Correction, Co-registration. 

### 2)[MONSTR](https://www.nitrc.org/projects/monstr)(Multi-cONtrast brain STRipping method )
- A software tool to generate brain masks (or skull-strip) from multi-contrast MR brain images, such as T1, T2, PD, or FLAIR. 
- Compared to other tools that are validated on T1-based skull stripping methods, MONSTR involves multi-modal inputs(supports T1, T2, FLAIR)와 multi-model atlases.
- Used for Skull Stripping.


## Step
### 1) Resampling
- Resize voxel to 1X1X1.
- Output
![alt_text](/readme_img/3_Resampling.gif)

### 2) N4 Bias Correction
- Method for correcting low frequency intensity non-uniformity present in MRI image data known as a bias or gain field.
- Output
![alt_text](/readme_img/4_Bias_correction.PNG)

### 3) Co-Registration (to T1C)
- Brings one image(mostly T1C) to match another image, such that the same voxels refers roughly to the same structure in both brains.
- Output
![alt_text](/readme_img/5_Co-registration.PNG)

### 4) Skull-Stripping + Apply skull mask
- Generate skull mask for each brain image, and strip.
- Output
![alt_text](/readme_img/6_Skull-stripping.PNG)
