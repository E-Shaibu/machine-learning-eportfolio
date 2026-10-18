# Individual Project Evidence: HOG-SVM versus CNN

## Project overview

This individual assignment, *Comparative Intelligence and Ethics in Machine Learning Systems*, investigated the performance, explainability, robustness and ethical implications of two approaches to waste-image classification: Histogram of Oriented Gradients combined with a Support Vector Machine (HOG-SVM), and a Convolutional Neural Network (CNN).

The project used the TrashNet dataset, containing 2,527 RGB images across six categories: cardboard, glass, metal, paper, plastic and trash.

## Model comparison

| Metric | HOG-SVM | CNN |
|---|---:|---:|
| Test accuracy | 62.1% | 54.7% |
| Macro precision | 64.6% | 57.1% |
| Macro recall | 58.1% | 57.0% |
| Macro F1-score | 59.8% | 52.8% |

HOG-SVM achieved stronger overall results in this experiment. However, class-level results showed that neither model performed best in every category. The CNN achieved a higher F1-score for cardboard, while HOG-SVM performed better for most of the other categories.

These findings demonstrate why model evaluation should consider multiple metrics and class-specific errors rather than accuracy alone.

## Robustness testing

A brightness perturbation was applied to the test images by increasing brightness by a factor of 1.25.

| Metric | HOG-SVM | CNN |
|---|---:|---:|
| Original accuracy | 62.1% | 54.7% |
| Accuracy after perturbation | 58.2% | 48.9% |
| Original macro F1 | 59.8% | 52.8% |
| Macro F1 after perturbation | 53.2% | 45.6% |

Both models experienced a performance decline. This suggests sensitivity to changes in illumination, although a single brightness experiment is insufficient to establish general robustness.

## Explainability and ethical considerations

The project considered Grad-CAM as an aid for examining CNN predictions. Such visualisations can help investigate image regions associated with model outputs, but they do not prove that a prediction is correct or that the model has learned meaningful material characteristics.

The dataset was also imbalanced: the trash category contained substantially fewer images than the paper category. This makes class-level evaluation particularly important, although class imbalance alone does not demonstrate demographic bias.

Potential deployment risks include incorrect material sorting, reduced recycling efficiency and additional manual work. Responsible deployment would require representative real-world testing, monitoring of class-specific errors, human oversight and procedures for correcting mistakes.

## Critical limitation

Test-set results were inspected during CNN fine-tuning. Therefore, the test set was not fully independent of the model-development process, and the reported test metrics should be interpreted cautiously. Future experiments should use validation data for model selection and reserve an untouched test set for final evaluation.

## Evidence status

This page summarises findings from my individual assignment presentation. Supporting figures, confusion matrices and explainability visualisations should be added where available, with captions identifying the experiment and its limitations.
