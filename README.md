# Fine-Tuning YOLOv11 for Enhanced Human Detection in Search and Rescue Missions

**MSc Data Science Thesis — South East Technological University, 2025**  
**Author:** Danial Nor Azman

---

## Overview

This repository contains the code, configuration, and documentation for my Master's thesis, which investigates the application of **YOLOv11**, the latest generation of the YOLO (You Only Look Once) real-time object detection architecture, to improve human detection accuracy in **search and rescue (SAR)** scenarios.

Missing persons in outdoor environments (forests, disaster zones, low-visibility terrain) are extremely difficult to detect using conventional methods. This research explores whether a fine-tuned YOLOv11 model can meaningfully improve detection rates under these challenging real-world conditions.

---

## Research Question

> *Can fine-tuning YOLOv11 on domain-specific search and rescue imagery significantly improve human detection performance compared to a baseline pre-trained model?*

---

## Repository Contents

```
Master_Thesis/
│
├── PROJECT.ipynb                        # Main notebook: training, evaluation, results
├── Nomad.yaml                           # Dataset configuration file
├── DanialNorAzman_C00253517_Thesis.pdf  # Full thesis document
├── Turnitin_Result.pdf                  # Originality report
└── README.md
```

> **Note:** Full image datasets and model weight files are stored externally on OneDrive due to file size constraints.  
> Dataset access: [OneDrive Link](https://setuo365-my.sharepoint.com/my?id=%2Fpersonal%2Fc00253517_setu_ie%2FDocuments%2FThesis&ga=1)

---

## Methodology

1. **Dataset Preparation**
   - Sourced and curated a labelled dataset of human figures in outdoor, low-visibility, and cluttered environments
   - Applied data augmentation techniques including flipping, brightness adjustment, and mosaic augmentation to improve model generalisation

2. **Model Fine-Tuning**
   - Used a pre-trained YOLOv11 model as the base
   - Fine-tuned on the domain-specific SAR dataset
   - Configured training via `Nomad.yaml` (epochs, batch size, image resolution, class labels)

3. **Evaluation**
   - Assessed model performance using standard object detection metrics: **mAP (mean Average Precision)**, **Precision**, **Recall**, and **F1-score**
   - Compared fine-tuned model against the baseline (pre-trained, no fine-tuning)
   - Tested across varied lighting conditions and scene complexity levels

---

## Key Findings

- Fine-tuning YOLOv11 on SAR-specific data produced measurable improvements in human detection accuracy over the baseline
- The model demonstrated stronger performance in cluttered environments where baseline detection failed
- Results suggest that domain-specific fine-tuning is a viable approach for deploying object detection models in specialised real-world contexts

---

## Technologies Used

| Category | Tools |
|---|---|
| Language | Python 3 |
| Deep Learning | YOLOv11 (Ultralytics), PyTorch |
| Data Handling | NumPy, Pandas |
| Visualisation | Matplotlib, OpenCV |
| Environment | Jupyter Notebook, Google Colab |
| Configuration | YAML |

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Danial-hakim/Master_Thesis.git
   ```

2. Install dependencies:
   ```bash
   pip install ultralytics torch torchvision numpy matplotlib opencv-python pandas
   ```

3. Download the dataset from the [OneDrive link](https://setuo365-my.sharepoint.com/my?id=%2Fpersonal%2Fc00253517_setu_ie%2FDocuments%2FThesis&ga=1) and place it in the project directory.

4. Open and run the notebook:
   ```bash
   jupyter notebook PROJECT.ipynb
   ```

---

## References & Background

- [YOLOv11 — Ultralytics Documentation](https://docs.ultralytics.com)
- Jocher, G. et al. (2023). Ultralytics YOLO. GitHub.
- Search and rescue detection datasets: Roboflow Universe SAR collections

---

## Author

**Danial Nor Azman**  
MSc Data Science — South East Technological University  
[GitHub](https://github.com/Danial-hakim) | [Portfolio](https://danial-hakim.github.io) | danialhakim01@gmail.com
