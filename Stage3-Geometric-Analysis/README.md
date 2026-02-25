# Stage 3: Geometric Correction & Advanced Deskewing

## 🎯 Overview
In this stage, the pipeline was upgraded to handle **severe geometric distortions**. We focused on solving the "High-Skew" problem where images are taken at sharp angles (e.g., 45°), which typically causes standard OCR to fail.

## 🛠 Key Enhancements
* **Advanced Deskewing:** Transitioned from basic **Bounding Box** logic to **Progressive Hough Transform** for text-line detection.
* **Geometric Rectification:** Implemented precise rotation based on detected text baselines rather than package edges.
* **Grayscale Optimization:** Refined the denoising step to work directly on grayscale rectified data for better character preservation.

## 🧪 Tested Scenarios
1. **Case 1 (Legacy Bounding Box):** Demonstrated how traditional geometric methods fail to distinguish between the package tilt and text orientation.
2. **Case 2 (Hough Transform Logic):** Successfully rectified a 45-degree tilted image, leading to accurate bilingual extraction.

## 🚀 How to Run
1. Open the `Stage_3_Geometric_Correction.ipynb` in **Google Colab**.
2. Run the **Environment Setup** cell to ensure all dependencies are installed.
3. Upload a severely tilted medicine label image (e.g., 45° angle) when prompted.
4. Execute the cells to compare the legacy vs. enhanced logic and view the final **Traffic Light Report**.
