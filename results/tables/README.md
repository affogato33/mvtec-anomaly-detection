# Experiment Tables

This folder contains the CSV files with the results from the experiments.

I have kept the results in separate files so it is easier to look at each part of the project without having to go through the entire notebook. The tables contains the full model results, category wise results, comparisons and statistical tests.

## Main Results

### Overall Results

File: `summary.csv`

This file has an overview of the main experiment results. It is useful for getting a quick idea of how the models performed.

### Model Performance

File: `metrics_all.csv`

This file contains the performance results collected across the experiments. It includes the different models and evaluation conditions.

### Model Family Comparison

File: `per_family.csv`

This file groups the results by model family. It makes it easier to compare the performance of different types of models.

## Additional Experiments

### Hypothesis Tests

File: `hypotheses.csv`

This file contains the results of the statistical tests used in the project.&#x20;

### Augmentation Transfer

File: `augmentation_transfer.csv`

This file contains the results from testing whether image augmentation helps the models perform better on image changes they have not seen during training.

### Exchangeability

File: `exchangeability.csv`

This file contains the results of the exchangeability checks carried out in the experiments.

### False Alarms

File: `false_alarms.csv`

This file contains the false alarm results. It helps compare how often the models identify normal images or regions as defective.

### Local Contrast

File: `followup_local_contrast.csv`

This file contains the results from the local contrast experiment. It looks at whether using local contrast along with the anomaly score can help reduce false alarms.

### Margin Sensitivity

File: `margin_sensitivity.csv`

This file contains the results from testing different margin settings. It helps check whether the evaluation results change when the margin is adjusted.

### Calibration

File: `test_split_calibration.csv`

This file contains the calibration results. It helps show how the selected thresholds affect false alarms and defect detection.

