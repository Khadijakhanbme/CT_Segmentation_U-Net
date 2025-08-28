# CT_Segmentation_U-Net
Automatic segmentation of lung lesions from CT scans is a critical step in understanding disease progression and assisting clinicians in treatment planning.
This project evaluates three deep learning architectures: U-Net, Attention U-Net, and Residual U-Net; for COVID-19 lung lesion segmentation using pre-processing and augmentation techniques.

## Highlights

### Dataset: [COVID-19 CT Scan Lesion Segmentation Dataset](https://www.kaggle.com/datasets/maedemaftouni/covid19-ct-scan-lesion-segmentation-dataset).
 

Models:

Traditional U-Net 

Attention U-Net with attention gates for small lesion focus 

Residual U-Net with skip and residual connections

Pre-processing:

Contrast enhancement with CLAHE and Gaussian smoothing 

Removal of empty masks & resizing (256×256, grayscale channels) 

Augmentation: Targeted flips and rotations, prioritizing small lesions 

Metrics: Dice Coefficient, Validation Accuracy, IOU
