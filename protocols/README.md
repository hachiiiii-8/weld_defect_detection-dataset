# Experimental protocols

This document summarizes the experimental settings reported in the WeldCDFNet manuscript.

## Main benchmark

- Input resolution: **640 × 640**, with letterbox resizing.
- Training: **200 epochs**, SGD, initial learning rate **0.01**, momentum **0.937**, weight decay **0.0005**, batch size **16**.
- Five independent runs: seeds **40, 41, 42, 43, 44**.
- Checkpoint selection: highest validation mAP@50:95 within each run.
- Inference confidence threshold: **0.25**; NMS IoU threshold: **0.70**.
- Reported metrics: Precision, Recall, mAP@50, mAP@50:95, parameters, FLOPs, model size, FPS.

## External evaluation

**Target-domain retraining:** five independently trained runs on each external dataset, retaining the corresponding official category definitions.

**Class-agnostic zero-shot:** models trained on the main source dataset are evaluated on external datasets without target-domain training or fine-tuning; source category predictions and defect ground-truth categories are collapsed to a foreground class for detection evaluation.

Datasets: PVIC-WELD, HWZO-WELD, MJHVT-WELD, NEU-DET, and GC10-DET.

## Perturbation evaluation

Six perturbations are considered: defocus blur, motion/vibration blur, low contrast, specular/arc glare, spatter/oxide contamination, and gamma/exposure correction. The original test set is L0, with L1–L4 defined by severity or exposure level. Models are evaluated without additional training or adaptation.

## Inference measurement

The main RTX 4090 FPS results were measured at batch size 1 after **50 warm-up** and **500 timed** iterations, including the processing steps described in the manuscript. Additional platform measurements include RTX 3060, CPU, and Jetson Orin Nano.

Evaluation scripts and model weights can be requested from the corresponding authors.
