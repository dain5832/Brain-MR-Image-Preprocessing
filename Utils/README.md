# Utils
### dcm_to_nii.ipynb
Convert dicom files to nifti.

### mask_preprocessing.ipynb
When resampled, each pixels of mask contains value in a range of 0-1.
By rounding up or down on 0.5, make those values only have either 0 or 1.

### organizing_files.ipynb
Organize(move, copy, and remove) files using pandas and os library.

### reorientation_final.ipynb
Convert orientation(corornal, sagittal, axial) of MR image and save it to new file. \
For more information, check out [affine transformation](https://nipy.org/nibabel/coordinate_systems.html).

### reorientation_task_20200924.ipynb
Working process of `reorientation_final.ipynb`.
