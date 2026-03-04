# Smart Medicine OCR System 💊

An advanced image processing pipeline designed to extract bilingual text (Arabic/English) from pharmaceutical labels with high accuracy.

## 🚀 Project Evolution (Stages)
The project is organized into sequential stages, each addressing specific technical challenges:

* **Stage1-Proposed-Pre-processing-Pipeline**
    * Implemented a pre-processing pipeline (Adaptive Scaling, Denoising, and Otsu’s Binarization) to handle **small fonts** and **background noise**, evaluated via a custom Traffic Light Reporting System.

* **Stage2-Bilingual-Analysis**
    * Integrated **Bilingual Recognition (ara+eng)**. Analyzed the engine’s behavior with different layouts, including parallel columns (interleaving) and the impact of unsupported scripts.

* **Stage3-Geometric-Analysis**
    * Solved **severe geometric distortions** using **Hough Transform** for text-line detection. Developed a robust rectification logic to handle images tilted up to 45 degrees.

## 🛠️ Key Technologies
* **OpenCV:** Image pre-processing and geometric transformations.
* **PyTesseract:** Bilingual text extraction (Arabic + English).
* **Python:** Core logic and pipeline integration.

## 📌 Current Status
The project has successfully stabilized noise, bilingual structure, and skewness issues. **Active development** is now focused on:
1.  **Lighting Resilience:** Implementing adaptive thresholding to neutralize shadows.
2.  **Structural Integrity:** Enhancing character thickness for more stable recognition.
