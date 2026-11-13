# Experiment Figures

This folder contains the main figures from the project. I have included these plots to make it easier to understand how the models performed and how different image changes affected their results.

## Main Figures

### Figure 1: Robustness Curves

File: `fig1_robustness_curves.png`

This figure shows how the models perform when different image changes are applied with increasing strength.

It helps us understand how quickly the performance drops as the images become more difficult to analyse. This image also lets us compare how the different models respond to these changes.

### Figure 2: Nuisance and Defect Comparison

File: `fig2_nuisance_vs_defect.png`

This figure looks at how image changes affect the model compared with actual defects in the images.

The motive is to see whether a model can still recognise defects when other changes are present. It also helps show whether certain image changes make it harder for the model to separate normal images from defective ones.

### Figure 3: Augmentation Transfer

File: `fig3_augmentation_transfer.png`

This figure compares the results of models trained with and without image augmentation.

One important part of the experiment was checking whether augmentation only helps with the changes used during training or whether it also helps with changes the model has not seen before.

The figure helps show the difference between these two cases.

### Figure 4: False Alarms

File: `fig4_false_alarms.png`

This figure focuses on false alarms during testing.

A false alarm happens when the model identifies a normal image or region as defective. This can become a problem when a model is used in a real world cases because too many false alarms can make the system less useful.

This figure also compares the false alarm results and helps us to understand how different methods affect them.

### Figure 5: NDR and Performance Drop

File: `fig5_ndr_predicts_drop.png`

This figure looks at the relationship between NDR and the drop in model performance.

It helps us examine whether NDR is related to how much performance changes when different image conditions are applied.

This gives another way to study how the models respond to changes in the input images.

### Figure 6: Local Contrast

File: `fig6_local_contrast.png`

This figure shows the results of using a local contrast score along with the anomaly scores.

The purpose was to check whether this additional score could reduce false alarms caused by changes in the images.

The results show that it can reduce false alarms on held out changes, but this also comes with a reduction in defect detection.&#x20;

## Category Visual Results

The `categories` folder contains visual examples from all 15 categories in the MVTec AD dataset.

The categories are:

1. Bottle
2. Cable
3. Capsule
4. Carpet
5. Grid
6. Hazelnut
7. Leather
8. Metal Nut
9. Pill
10. Screw
11. Tile
12. Toothbrush
13. Transistor
14. Wood
15. Zipper

They make it easier to see how the models behave across different types of objects and textures.

