# Mini AI Pipeline: Day vs Night Classification

**CAS2105 Mini AI Pipeline Project**

_Student Name: Minji Jung_
_Student ID: 2023149028_

## Project Structure

This repository contains the dataset, source code, and final report for the Day/Night Image Classification task.

- `CAS2105__Homework_6_Submission_2023149028.pdf`: The final project report.
- **`dataset/`**: Contains processed Day/Night images (Standardized JPG format).
- **`notebooks/`**:
  - `day_night_classifier.ipynb`: **[Main]** The main pipeline code (Baseline vs. AI Model). Run this to reproduce the results.
  - `preprocessing.ipynb`: **[Reference]** Preprocessing logs showing how raw images (avif, webp) were converted to standard JPG.
- **`requirements.txt`**: Python dependencies.

## AI Pipeline Details (`day_night_classifier.ipynb`)

The main notebook is organized into the following sections:

1.  **Imports & Setup**: Loads necessary libraries (Transformers, PIL, etc.).
2.  **Dataset Loading**: Loads images from the `dataset/` folder and assigns ground truth labels (Day=0, Night=1).
3.  **Naïve Baseline**: Implements the brightness threshold (avg > 120) logic.
4.  **AI Pipeline (CLIP)**: Performs zero-shot inference using the pre-trained CLIP model.
5.  **Evaluation**: Computes accuracy metrics for both methods. (Baseline vs CLIP)
6.  **Qualitative Examples**: Visualizes specific images where the Baseline or AI model (CLIP) failed (as discussed in the report).

## Installation & Usage

### 0. Environment

All experiments were conducted in a standard Python environment
(Linux, Python 3.8+).
To reproduce the results, please install the dependencies:

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Run the notebook

Open `notebooks/day_night_classifier.ipynb` and run all cells.
