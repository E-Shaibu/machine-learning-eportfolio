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

- **Individual project presentation:** [Comparative Intelligence and Ethics in Machine Learning](./COMPARATIVE%20INTELLIGENCE%20%20AND%20ETHICS%20IN%20MACHINE%20LEARNING2%20%20%20.ppt)
- **Experimental notebook:** [ML vs DL notebook](./ML%20vs%20DL.ipynb)

The presentation summarises the comparison between HOG-SVM and CNN, including model performance, brightness robustness, explainability and ethical considerations. The notebook contains supporting experimental code and outputs.
## Reflection
What did this experiment teach me about comparing models beyond accuracy? What would I change in the experimental design before deployment?
