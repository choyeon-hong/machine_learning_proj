# Liver Cancer Grade Classification using Machine Learning

In this project, I developed a machine learning model to classify liver cancer grades into four classes:

* RN & Low grade DN
* High grade DN
* HCC in DN
* Progressed HCC

The workflow handles high-resolution pathology images and transforms them into a structured dataset suitable for machine learning algorithms.

---

## Approach

### 1. Patch Extraction

Pathology slides of liver cancer are usually stored as large whole-slide images (WSIs). They are too large to feed directly into many ML models. 
From WSIs in `.svs` format, 1024×1024 patches are generated based on regions of interest.

### 2. Feature Extraction

Using tools such as CellProfiler and QuPath, each patch is converted into numerical features. This simplifies image-based classification into machine learning tasks.

### 3. Pre-processing

Since the extracted features have different numerical ranges and units, a Standard Scaler is applied.
To reduce dimensionality and eliminate redundant or irrelevant features, feature selection techniques are applied.

### 4. Model Training

Extracted features are used to train a machine learning classifier to distinguish between cancer classes.

* Data are not shared in this repository.

---

## Pipeline

```
image data -> feature extraction -> Pre-processing -> training ML models -> validation -> visualization
```
