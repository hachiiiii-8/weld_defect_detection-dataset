# Weld defect dataset

The benchmark described in the WeldCDFNet manuscript contains **6,190 images**, **28,921 annotated instances**, and **nine defect classes**: air-hole, pore, stain, discontinuity, deposit, overlap, hollow-bead, unfused, and broken-arc.

**Dataset archive:** [weld-dataset.zip (Google Drive)](https://drive.google.com/file/d/19eFmz3DzF9db0GrNssFRj7Yi4IXCsgWw/view?usp=drivesdk).

## Data sources

| Source | Images | Annotated instances | Independent groups |
| --- | ---: | ---: | ---: |
| Steel | 3,168 | 11,694 | 473 |
| Weld-Low | 2,000 | 8,718 | 226 |
| Weld-High | 736 | 6,204 | 159 |
| Robot platform | 286 | 2,305 | 37 |
| **Total** | **6,190** | **28,921** | **895** |

The reported split is **4,333/619/1,238 images** for training/validation/testing, respectively, with **20,704/2,304/5,913** annotated instances. The corresponding independent-group counts are **625/91/179**.

Images from the same weld scene, workpiece, welding run, or acquisition sequence are assigned to the same subset. Matching low- and high-resolution observations are grouped together.

## Class distribution

| Class | Instances |
| --- | ---: |
| air-hole | 5,191 |
| pore | 4,155 |
| stain | 8,307 |
| discontinuity | 7,220 |
| deposit | 2,730 |
| overlap | 223 |
| hollow-bead | 229 |
| unfused | 408 |
| broken-arc | 458 |
| **Total** | **28,921** |

The manuscript describes annotations in YOLO detection format. Refer to the linked archive for its actual packaged files.
