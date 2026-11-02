# WeldCDFNet

**Lightweight Contextual Dynamic Fusion for Robust Weld Defect Detection in Complex Industrial Images**

WeldCDFNet is a lightweight weld defect detector built on YOLOv13n. It combines multi-scale contextual representation, Fourier-based cross-scale alignment, and content-adaptive localization to detect weak and irregular defects in complex metallic images.

## Method

| Component | Main operation | Location |
| --- | --- | --- |
| **PBNet** | Multi-scale contextual modeling and local-texture enhancement | Backbone |
| **C-FAAF** | Fourier orientation estimation and component-wise feature alignment | Cross-scale fusion |
| **CMDetect** | Regional affinity modeling and dynamic localization kernels | Detection head |

## Dataset

The weld defect benchmark includes **6,190 images**, **28,921 annotated instances**, and **nine defect categories** from four sources.

| Source | Images |
| --- | ---: |
| Steel | 3,168 |
| Weld-Low | 2,000 |
| Weld-High | 736 |
| Robot platform | 286 |
| **Total** | **6,190** |

**[Download weld-dataset.zip (Google Drive)](https://drive.google.com/file/d/19eFmz3DzF9db0GrNssFRj7Yi4IXCsgWw/view?usp=drivesdk)**

The reported scene-grouped split contains **4,333 training**, **619 validation**, and **1,238 test** images. Dataset sources, class statistics, and group counts are described in [data/README.md](data/README.md).

## Main results

| Detector | Precision (%) | Recall (%) | mAP@50 (%) | mAP@50:95 (%) | Parameters (M) | GFLOPs | FPS |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| YOLOv13n | 81.7 ± 0.23 | 80.7 ± 0.34 | 82.2 ± 0.12 | 52.7 ± 0.23 | 2.46 | 6.2 | 72 |
| **WeldCDFNet** | **85.7 ± 0.14** | **82.9 ± 0.12** | **86.8 ± 0.10** | **55.1 ± 0.11** | **2.44** | **6.1** | 67 |

Accuracy is reported as mean ± standard deviation across **five independent runs** (seeds **40, 41, 42, 43, 44**). The FPS values are measured on an RTX 4090 at 640 × 640 input and batch size 1.

## Reproducibility resources

| Resource | File |
| --- | --- |
| Dataset download | [weld-dataset.zip](https://drive.google.com/file/d/19eFmz3DzF9db0GrNssFRj7Yi4IXCsgWw/view?usp=drivesdk) |
| Dataset description and class distribution | [data/README.md](data/README.md) |
| Split image, instance, and group counts | [data/split_summary.csv](data/split_summary.csv) |
| Paper-reported training settings | [configs/training.yaml](configs/training.yaml) |
| Paper-reported evaluation settings | [protocols/evaluation.yaml](protocols/evaluation.yaml) |
| Source-wise dataset statistics | [records/source_statistics.csv](records/source_statistics.csv) |
| Defect-category instance counts | [records/class_counts.csv](records/class_counts.csv) |

## Model weights

For trained WeldCDFNet model weights, please contact the corresponding authors.
