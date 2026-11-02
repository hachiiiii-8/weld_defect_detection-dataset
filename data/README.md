# Weld defect dataset

The weld benchmark comprises **6,190 images**, **28,921 selected defect annotations**, and **nine defect categories** from Steel and LoHi-WELD.

**Dataset archive:** [weld-dataset.zip (Google Drive)](https://drive.google.com/file/d/19eFmz3DzF9db0GrNssFRj7Yi4IXCsgWw/view?usp=drivesdk).

## Source collections

| Collection | Images | Selected source-native annotations |
| --- | ---: | ---: |
| Steel | 3,168 | 6,509 |
| LoHi-WELD | 3,022 | 22,412 |
| **Total** | **6,190** | **28,921** |

LoHi-WELD contains **2,000 low-resolution** and **1,022 high-resolution** robotic-welding images.

## Selected native categories

| Defect category | Steel | LoHi-WELD |
| --- | ---: | ---: |
| air-hole | 5,191 | — |
| pore | — | 3,950 |
| stain | — | 8,307 |
| discontinuity | — | 7,220 |
| deposit | — | 2,935 |
| overlap | 223 | — |
| hollow-bead | 229 | — |
| unfused | 408 | — |
| broken-arc | 458 | — |
| **Total** | **6,509** | **22,412** |

The table reports selected annotations in the original datasets' category systems. The standardized benchmark category totals are available in [records/class_counts.csv](../records/class_counts.csv).

## Evaluation split

The reported image split is **4,333 training**, **619 validation**, and **1,238 test** images, containing **20,704**, **2,304**, and **5,913** annotated instances, respectively. Source-linked scene observations, including corresponding LoHi-WELD resolution variants, are kept within the same subset.
