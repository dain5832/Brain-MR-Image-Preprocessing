# Brain_Raw

### Dcm to Nii
convert dcm files to nifti

### file_manipulation
manipulate file using pandsa and os module(move, copy, remove)

### get_axial_slice_from_sagittal
Convert plane(corornal, sagittal, axial) of MR image and save it to new file

### Meningioma Preprocessing
Preprocess Brain MR Image nifti files

#### Step
1) Resampling
2) N4 Bias Correction
3) Co-Registration (to T1C)
4) Skull-Stripping

#### Tools
1) ANTs
- Resampling, N4 Bias Correction
2) MONSTR
- Co-Registration, Skull-Stripping
