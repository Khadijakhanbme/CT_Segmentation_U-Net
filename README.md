# CT Lung Lesion Segmentation (COVID-19) with U-Net Variants  

Automatic segmentation of lung lesions from CT scans is a critical step in understanding disease progression and assisting clinicians in treatment planning. This project evaluates three deep learning architectures: **U-Net, Attention U-Net, and Residual U-Net** for COVID-19 lung lesion segmentation using preprocessing and augmentation techniques.  

---

## Highlights
- **Dataset**: [COVID-19 CT Scan Lesion Segmentation Dataset](https://www.kaggle.com/datasets/maedemaftouni/covid19-ct-scan-lesion-segmentation-dataset)
  <img width="801" height="522" alt="image" src="https://github.com/user-attachments/assets/faf5e8e2-ee92-428f-9b6b-59e1c786c1d2" />

- **Models**:  
  - Traditional **U-Net**  
  - **Attention U-Net** (with attention gates to capture small lesions)  
  - **Residual U-Net** (skip + residual connections)  
- **Metrics**: Dice Coefficient, Validation Accuracy, IOU  

---

##  Preprocessing
To improve lesion visibility and training efficiency:  
- Applied **CLAHE** (Contrast Limited Adaptive Histogram Equalization)  
- **Gaussian smoothing** to reduce noise  
- Removed empty masks for cleaner training  
- Resized CT images → `256×256` grayscale  
- Normalized pixel intensity values (0–1)  

---

## Data Augmentation
Since small lesions are harder to detect, augmentation focused on preserving them:  
- Horizontal & vertical flips  
- Random rotations  
- Scaling & slight translations  

This helped the models generalize better and reduced overfitting.  

---

## 📊 Results (Summary)
- **U-Net**: Strong baseline, struggled with small lesions  
- **Attention U-Net**: Best performance, captured both large and small lesions  
- **Residual U-Net**: Competitive results, but less consistent than Attention U-Net  

---

## Outputs

**Original CT | Pre-processed Slices | Ground Truth**  

<img width="915" height="617" alt="image" src="https://github.com/user-attachments/assets/96a7cfdb-e2b7-4b51-95af-42923ac2b8dc" />

---


**Original CT | Ground Truth | Attention Unet | Unet | Residual Unet**  

<img width="1004" height="650" alt="image" src="https://github.com/user-attachments/assets/66825936-48e9-4053-9048-aaa922d6bde9" />

---


**Training Curves: Attention U-Net | Conventional U-Net | Residual U-Net|**  

<img width="966" height="437" alt="image" src="https://github.com/user-attachments/assets/76e44a56-830f-48be-b62a-f0dff8bd02a8" />
<img width="952" height="556" alt="image" src="https://github.com/user-attachments/assets/a79b4ceb-09d2-425f-9f35-3bccd9933596" />
<img width="982" height="542" alt="image" src="https://github.com/user-attachments/assets/9816bb98-5937-45ca-8363-1c8a6a0c6817" />


---

## Significance & Future Work

**Significance:**  
- Supports development of **automated tools** for early and precise diagnosis of lung diseases like COVID-19.  
- Can **reduce manual workload** for radiologists and improve clinical efficiency.  

**Future Directions:**  
- Apply hybrid architectures and loss functions to improve **small lesion detection** and **boundary accuracy**.  
- Extend the approach to **other medical imaging datasets** to generalize applicability.   


## References

- Ronneberger et al., *U-Net: Convolutional Networks for Biomedical Image Segmentation*, MICCAI, 2015  
- P. Gifani, A. Shalbaf, and M. Vafaeezadeh, *Automated detection of COVID-19 using ensemble of transfer learning with deep convolutional neural network based on CT scans*, Int J Comput Assist Radiol Surg, 2021  
- S. Saifullah, A. Pranolo, and R. Dreżewski, *Comparative Analysis of Image Enhancement Techniques for Brain Tumor Segmentation: Contrast, Histogram, and Hybrid Approaches*, E3S Web of Conferences, 2024  
- B. Shirokikh et al., *Universal Loss Reweighting to Balance Lesion Size Inequality in 3D Medical Image Segmentation*, LNCS, 2020  

---

## 👩‍💻 Author
**Khadija Khan**  
MSc Biomedical Engineering  


