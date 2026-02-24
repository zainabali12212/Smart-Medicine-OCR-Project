# Stage 2: Bilingual Support & Structural Analysis Tuning

## 🎯 Overview
In this stage, the OCR pipeline was enhanced to support **Arabic and English** scripts simultaneously. We moved beyond simple image processing to analyze how text layout (Parallel vs. Linear) and unsupported scripts (e.g., Hindi) affect extraction accuracy.

## 🛠 Key Enhancements
* **Bilingual Configuration:** Integrated `tesseract-ocr-ara` and configured the engine for `ara+eng`.
* **Structural Tuning:** Applied Page Segmentation Mode (`PSM 3`) for automatic layout analysis.
* **Layout Testing:** Evaluation of "Structural Interleaving" in parallel columns vs. success in linear layouts.

## 🧪 Tested Scenarios
1.  **Case 1 (Parallel Columns):** Analyzed "Line Interleaving" where Arabic and English text appear in side-by-side columns.
2.  **Case 2 (Linear Layout):** Verified high-accuracy extraction in vertical layouts and observed how the engine handles unsupported scripts (Hindi).

## 🚀 How to Run
1. Open the `Stage2_Bilingual_Structural_Tuning.ipynb` in **Google Colab**.
2. Run the **Environment Setup** cell to install the Arabic language pack.
3. Upload a bilingual medicine label image when prompted.
4. Execute the processing cells to view the visual stages and the final extracted text report.
