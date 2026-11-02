# WeldCDFNet

**Lightweight Contextual Dynamic Fusion for Robust Weld Defect Detection in Complex Industrial Images**

WeldCDFNet is a lightweight detector based on YOLOv13n for industrial weld-surface inspection. It combines contextual feature extraction, Fourier-domain cross-scale alignment, and content-adaptive localization to detect small, low-contrast, and irregular defects under complex metallic backgrounds.

## Method

| Component | Main operation | Location |
| --- | --- | --- |
| **PBNet** | Multi-scale contextual modeling and local-texture enhancement | Backbone |
| **C-FAAF** | Local Fourier orientation estimation, component alignment, and attention-based fusion | Cross-scale feature fusion |
| **CMDetect** | Regional affinity modeling and spatially varying dynamic kernels | Detection-head localization branch |

## Weld defect dataset

The benchmark reported in the manuscript contains **6,190 images**, **28,921 annotated defect instances**, and **nine categories** from four acquisition sources.

| Source | Images |
| --- | ---: |
| Steel | 3,168 |
| Weld-Low | 2,000 |
| Weld-High | 736 |
| Robot platform | 286 |
| **Total** | **6,190** |

**[Download the weld dataset archive (Google Drive)](https://drive.google.com/file/d/19eFmz3DzF9db0GrNssFRj7Yi4IXCsgWw/view?usp=drivesdk)**

The reported scene-grouped partition contains **4,333 training**, **619 validation**, and **1,238 test** images. Source and grouping statistics, class names, and annotation totals are documented in [data/README.md](data/README.md).

## Main benchmark

| Detector | Precision (%) | Recall (%) | mAP@50 (%) | mAP@50:95 (%) | Params (M) | GFLOPs | FPS |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| YOLOv13n | 81.7 ± 0.23 | 80.7 ± 0.34 | 82.2 ± 0.12 | 52.7 ± 0.23 | 2.46 | 6.2 | 72 |
| **WeldCDFNet** | **85.7 ± 0.14** | **82.9 ± 0.12** | **86.8 ± 0.10** | **55.1 ± 0.11** | **2.44** | **6.1** | 67 |

Detection accuracy is reported as the mean ± standard deviation over five independent runs, using random seeds **40–44**. FPS refers to direct RTX 4090 measurements with an input size of 640 × 640 and a batch size of 1.

## External evaluation

Two evaluation protocols cover five external datasets: **PVIC-WELD, HWZO-WELD, MJHVT-WELD, NEU-DET**, and **GC10-DET**.

| Protocol | WeldCDFNet overall mAP@50 (%) | Best compared baseline (%) |
| --- | ---: | ---: |
| Five-run target-domain retraining | **79.7** | 78.1 |
| Five-checkpoint class-agnostic zero-shot transfer | **45.2** | 41.4 |

The zero-shot metric evaluates defect-region localization across different category systems. Further outcome summaries are in [results/README.md](results/README.md).

## Experimental protocol and resources

- [Dataset sources, annotations, and reported split](data/README.md)
- [Training and evaluation protocols](protocols/README.md)
- [Main and external evaluation results](results/README.md)

Evaluation scripts and trained WeldCDFNet model weights are available from the corresponding authors upon reasonable request.

## Paper

*WeldCDFNet: Lightweight Contextual Dynamic Fusion for Robust Weld Defect Detection in Complex Industrial Images.*

