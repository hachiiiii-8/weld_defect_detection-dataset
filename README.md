# WeldCDFNet

**WeldCDFNet: Lightweight Contextual Dynamic Fusion for Robust Weld Defect Detection in Complex Industrial Images**

WeldCDFNet is a lightweight YOLOv13n-based model for detecting weld defects in industrial images.

## Method

- **PBNet:** Multi-scale contextual and local-texture feature extraction.
- **C-FAAF:** Fourier-domain orientation estimation and cross-scale feature alignment.
- **CMDetect:** Content-adaptive dynamic convolution in the localization branch.

## Dataset

The weld defect benchmark contains **6,190 images**, **28,921 annotated instances**, and **nine defect categories**. Its training, validation, and test subsets contain **4,333**, **619**, and **1,238** images, respectively.

**[Download weld-dataset.zip (Google Drive)](https://drive.google.com/file/d/19eFmz3DzF9db0GrNssFRj7Yi4IXCsgWw/view?usp=drivesdk)**

See [dataset information](data/README.md) for source and class statistics.

## Main results

| Model | mAP@50 (%) | mAP@50:95 (%) | Parameters (M) | GFLOPs |
| --- | ---: | ---: | ---: | ---: |
| YOLOv13n | 82.2 ± 0.12 | 52.7 ± 0.23 | 2.46 | 6.2 |
| **WeldCDFNet** | **86.8 ± 0.10** | **55.1 ± 0.11** | **2.44** | **6.1** |

Results are reported over five independent runs using seeds **40, 41, 42, 43, and 44**.

## Code and model weights

For the paper's code and trained model weights, please feel free to contact the corresponding authors.
