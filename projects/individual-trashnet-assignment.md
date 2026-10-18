# Individual Assignment — Comparative Intelligence and Ethics in Machine Learning

**Project:** Comparison of HOG-SVM and CNN for TrashNet waste-image classification  
**Evidence:** Individual presentation and associated experiment outputs.

## Aim
Compare a traditional machine-learning pipeline using Histogram of Oriented Gradients (HOG) features and an SVM with a convolutional neural network (CNN), considering performance, explainability, robustness and responsible deployment.

## Dataset and method
Document the dataset, class distribution, train/validation/test split, preprocessing, model configurations and evaluation approach using the actual assignment materials.

## Reported results
The presentation reports:
- HOG-SVM test accuracy: 62.1%; macro F1: 59.8%.
- CNN test accuracy: 54.7%; macro F1: 52.8%.
- Under the tested brightness transformation, HOG-SVM accuracy changed from 62.1% to 58.2%, and CNN accuracy from 54.7% to 48.9%.

These results apply to this experiment only. The presentation notes that the test set was inspected during CNN fine-tuning, so it was not fully independent for final evaluation.

## Explainability and ethics
Describe the Grad-CAM analysis and the implications of class-level errors, dataset limitations, brightness sensitivity and the need for independent evaluation and human oversight.

## Artefacts
- Presentation: add a link to the file or published copy.
- Notebook/results: add links or selected screenshots where appropriate.
- Confusion matrix/Grad-CAM/robustness evidence: add verified images.

## Reflection
What did this experiment teach me about comparing models beyond accuracy? What would I change in the experimental design before deployment?
