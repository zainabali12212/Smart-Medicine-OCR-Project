# Smart Medicine OCR System 💊

An advanced image processing pipeline designed to extract bilingual text (Arabic/English) from pharmaceutical labels with high accuracy.

## 🚀 Project Evolution (Stages)
The project is organized into sequential stages, each addressing specific technical challenges:

* **[Stage 1: Handling Noise & Scale](./Stage1)**
    * Focused on **Noise & Scale Interference**. Addressed background textures and the mix of large brand names with tiny dosage info.
* **[Stage 2: Bilingual & Structural Complexity](./Stage2)**
    * Focused on **Arabic/English Support**. Solved the failure to analyze parallel multi-language columns and non-Latin scripts.
* **[Stage 3: Layout & Skew Correction](./Stage3)**
    * Focused on **Skewed Layouts**. Implemented geometric analysis to fix tilted or rotated labels that disrupt the reading path.

## 🛠️ Key Technologies
* **OpenCV:** Image pre-processing and geometric transformations.
* **PyTesseract:** Bilingual text extraction (Arabic + English).
* **Python:** Core logic and pipeline integration.

## 📌 Current Status
The project has successfully solved noise, bilingual structure, and orientation issues. **Active development** is now focused on:
1.  **Lighting Resilience:** Using adaptive techniques to neutralize shadows.
2.  **Structural Integrity:** Normalizing font weight to improve recognition.
