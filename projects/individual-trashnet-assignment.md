# Individual Assignment: Comparative Intelligence and Ethics in Machine Learning

**Project:** Comparing HOG-SVM and CNN for TrashNet waste-image classification  
**Focus:** Model performance, robustness, explainability and responsible AI.

## Project Overview

The aim of this project was to compare a traditional machine-learning approach, using Histogram of Oriented Gradients (HOG) features and a Support Vector Machine (SVM), with a Convolutional Neural Network (CNN) for waste-image classification.

The project examined predictive performance, robustness to brightness changes, explainability and the ethical considerations involved in deploying image-classification systems.

## Dataset and Methodology

I used the TrashNet dataset, containing 2,527 RGB images across six waste categories: cardboard, glass, metal, paper, plastic and trash. The dataset was divided into 1,768 training images, 379 validation images and 380 test images.

The HOG-SVM model used extracted image features, with the SVM regularisation parameter selected through validation macro F1-score. The CNN learned image features during training. Both approaches were evaluated using accuracy, precision, recall and macro F1-score. I also investigated the effect of a brightness transformation on classification performance.

## Results and Comparison

| Metric | HOG-SVM | CNN |
|---|---:|---:|
| Test accuracy | 62.1% | 54.7% |
| Macro precision | 64.6% | 57.1% |
| Macro recall | 58.1% | 57.0% |
| Macro F1-score | 59.8% | 52.8% |

HOG-SVM achieved better overall accuracy and macro F1-score in my experiments. However, class-level results revealed a more nuanced picture: the CNN achieved higher recall for the trash category, although its precision for that category was low.

Both models were affected by the brightness transformation. HOG-SVM accuracy decreased from 62.1% to 58.2%, while CNN accuracy decreased from 54.7% to 48.9%. This highlighted the importance of testing models under different image conditions rather than relying exclusively on results from the original dataset.

## Explainability, Ethics and Limitations

The project considered Grad-CAM for examining image regions that contribute to CNN predictions. It also highlighted the implications of class imbalance, classification errors and sensitivity to image conditions.

An important limitation was that the test set was inspected during CNN fine-tuning. Consequently, it was not fully independent for final evaluation. In future experiments, I would use validation data for model selection and reserve the test set for final evaluation only. Further testing under realistic lighting and deployment conditions would also be necessary.

## Reflection

This project taught me that model selection involves more than choosing the model with the highest accuracy. Although HOG-SVM performed better overall in my experiment, the CNN's class-level recall demonstrated that different models may be preferable depending on the practical consequences of prediction errors.

I also learned that robustness, explainability and evaluation methodology are essential to responsible AI. In future projects, I would strengthen the experimental design, investigate class-level errors more extensively and ensure that evaluation data remains independent of model-development decisions.

## Artefacts

- [Individual project presentation](./COMPARATIVE%20INTELLIGENCE%20%20AND%20ETHICS%20IN%20MACHINE%20LEARNING2%20%20%20.ppt)
- [Experimental notebook: ML vs DL](./ML%20vs%20DL.ipynb)

The presentation contains the project discussion and reported findings, while the notebook provides supporting experimental code and outputs.

## References
Dalal, N. and Triggs, B. (2005) ‘Histograms of oriented gradients for human detection’, Proceedings of CVPR, Vol. 1, pp. 886–893. https://doi.org/10.1109/CVPR.2005.177

Cortes, C. and Vapnik, V. (1995) ‘Support-vector networks’, Machine Learning, 20, pp. 273–297. https://doi.org/10.1007/BF00994018

Thung, G. and Yang, M. (2016) Classification of Trash for Recyclability Status. Stanford University, CS229 project report. https://cs229.stanford.edu/proj2016/report/ThungYang-ClassificationOfTrashForRecyclabilityStatus-report.pdf 

Thung, G. (n.d.) TrashNet dataset. Hugging Face. https://github.com/garythung/trashnet 
