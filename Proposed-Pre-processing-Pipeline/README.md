# Proposed Pre-processing Pipeline: Experimental Results

This directory contains the experimental setup and results for **Stage 1** of the Smart Medicine OCR project. The focus of this stage is to evaluate the effectiveness of a custom image enhancement pipeline on various medicine label challenges.

## 🛠 Experimental Setup
The pipeline consists of four main technical stages designed to optimize text clarity before it reaches the OCR engine:
1. **Adaptive Scaling (2x):** Increasing resolution to capture fine details in small fonts.
2. **Grayscale Conversion:** Reducing color complexity to focus on structural text features.
3. **Advanced Denoising:** Using Non-Local Means Denoising to remove sensor noise and artifacts.
4. **Otsu’s Binarization:** Automatically determining the optimal threshold for a clean black-and-white output.

## 🧪 Tested Scenarios (Cases)
The notebook demonstrates the pipeline's performance across three distinct scenarios:

* **Case 1: Small Font Recognition (Scaling)**
    * *Challenge:* Text like "100 Tablets" was too small for standard OCR.
    * *Result:* 2x scaling successfully enabled clear extraction.
* **Case 2: Noisy Backgrounds (Denoising)**
    * *Challenge:* Textured labels created "salt and pepper" noise.
    * *Result:* Denoising cleared the background, though some faint characters required strict thresholding.
* **Case 3: Multi-Scale Text (Scale Interference)**
    * *Challenge:* Handling images where titles are very large and secondary details are very small.
    * *Observation:* Examines the impact of a uniform scaling factor on diverse font sizes within a single frame.

## 🚦 Traffic Light Reporting System
To evaluate quality, each case generates a status report:
- 🟢 **GREEN:** High-confidence extraction.
- 🟡 **YELLOW:** Detected noise or potential character misidentification.
- 🔴 **RED:** OCR failed to identify meaningful text.

## 🚀 How to Run
1. Open the `.ipynb` file in **Google Colab**.
2. Run the initialization cell to install `Tesseract-OCR` and dependencies.
3. Download the test images from this folder, then upload them when prompted in each Case section.
