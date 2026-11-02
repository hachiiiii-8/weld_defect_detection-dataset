# Reported results

The values below are drawn from the WeldCDFNet manuscript and summarize the published evaluation protocols.

## Main weld-detection benchmark

| Model | Precision (%) | Recall (%) | mAP@50 (%) | mAP@50:95 (%) | Params (M) | GFLOPs | FPS |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| YOLOv13n | 81.7 ± 0.23 | 80.7 ± 0.34 | 82.2 ± 0.12 | 52.7 ± 0.23 | 2.46 | 6.2 | 72 |
| **WeldCDFNet** | **85.7 ± 0.14** | **82.9 ± 0.12** | **86.8 ± 0.10** | **55.1 ± 0.11** | **2.44** | **6.1** | 67 |

The accuracy values are mean ± standard deviation across five independent runs.

## External datasets

| Dataset | Target-domain retraining mAP@50 (%) | Class-agnostic zero-shot mAP@50 (%) |
| --- | ---: | ---: |
| PVIC-WELD | 77.2 ± 0.41 | 48.7 ± 0.48 |
| HWZO-WELD | 72.2 ± 0.58 | 44.6 ± 0.66 |
| MJHVT-WELD | 82.0 ± 0.38 | 54.2 ± 0.55 |
| NEU-DET | 87.9 ± 0.26 | 41.0 ± 0.42 |
| GC10-DET | 79.0 ± 0.47 | 37.6 ± 0.50 |
| **Overall macro mean** | **79.7** | **45.2** |

## Hardware

For the complete WeldCDFNet, the manuscript reports **67 FPS** on RTX 4090 and **15.8 FPS** on Jetson Orin Nano under the tested configurations.
