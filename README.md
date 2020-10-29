# Brain_MR_Image_Processing

## dcm_ti_nii.ipynb
Convert dicom files to nifti


## file_manipulation.ipynb
Manipulate(move, copy, and remove) file using pandas and os library


## get_axial_slice_from_sagittal.ipynb
Convert plane(corornal, sagittal, axial) of MR image and save it to new file


## Meningioma_Preprocessing,ipynb
Preprocess Brain MR Image nifti files

### Step
1) Resampling
2) N4 Bias Correction
3) Co-Registration (to T1C)
4) Skull-Stripping

### Tools
1) ANTs
- Resampling, N4 Bias Correction
2) MONSTR
- Co-Registration, Skull-Stripping
