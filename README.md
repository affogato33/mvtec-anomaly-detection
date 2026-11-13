# MVTec Anomaly Detection

This project is about how well computer vision models can find defects in images when the images are changed in different ways.

I used the MVTec AD dataset and tested different versions of PatchCore and PaDiM. I then looked at how changes in lighting, colour, noise, blur and image angle, can in turn, affect the results.

The main motive was to understand whether a model that works well on normal images can still find defects when the images look different from what it was trained on.

## Dataset

The dataset is MVTec Anomaly Detection dataset.

It contains 15 categories of objects and textures. Each category has normal images and also images with defects.

## Models

The experiments has seven detector configurations based on:

1. PatchCore with WRN50
2. Augmented PatchCore
3. PatchCore with photometric normalisation
4. PatchCore with DINOv2 features
5. PaDiM with WRN50
6. Augmented PaDiM
7. Additional model and feature comparisons included in the notebook

## What was tested

The models were tested under different image conditions:

1. Changes in brightness and gamma
2. Changes in colour temperature
3. Gaussian noise
4. Motion blur
5. JPEG compression
6. Rotation
7. Perspective changes

I also compared changes that were included during training with changes the models had not seen before.

## Main Results

| Evaluation             | Baseline PatchCore | Augmented PatchCore |
| ---------------------- | -----------------: | ------------------: |
| Clean image AUROC      |             0.9882 |              0.9878 |
| Seen shift image AUROC |             0.8848 |              0.9679 |
| Held out image AUROC   |             0.8651 |              0.8756 |
| Held out pixel AUROC   |             0.9231 |              0.9252 |
| Held out AUPRO         |             0.7826 |              0.7910 |

Augmentation helped the model perform better on changes it had seen during training. The improvement on new changes was much smaller.

The experiments also showed that reducing false alarms can come with a loss in defect detection. This means that a model needs to balance both.

## Results and Figures

The `results` folder contains the experiment tables and figures.

The `results/tables` folder contains the CSV files with the measured results.

The `results/figures` folder contains the main plots and visual examples from the experiments.

## Deployment Tests

I also tested the feature extractor with ONNX and compared its output with PyTorch.

A C++ inference test was compiled and run to check whether the exported model could be used outside the original Python setup.

## Limitations

The experiments use a single training seed.

Good performance on changes seen during training does not guarantee good performance on new changes.

## Tools Used

Python, PyTorch, OpenCV, NumPy, Pandas, Matplotlib, ONNX and C++.
