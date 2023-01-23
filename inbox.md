# Inbox

# statistics

## Binary classification

Confusion matrix
 TP, FP, FN and TN are the number of true positives, false positives, false negatives and true negatives respectively.

 Precision = TP / (TP + FP)
  the proportion of true positives out of all detected positives

Recall = TP / (TP + FN)
    the proportion of true positives out of all actual positives

 F1-score is the harmonic mean of the precision and recall. It is a good measure to use if you have an uneven class distribution (uneven number of positive and negative classes).

 Accuracy is the proportion of samples that are correctly classified. It is a good measure to use if you have symmetric datasets (equal number of positive and negative classes).

  "issues with the classic metrics: accuracy is sensitive to class imbalance; precision, recall, and F1-score are asymmetric. So what’s one to do? If both classes are of interest, one can treat a binary classification problem as a multi-class problem with 2 classes, and then calculate the corresponding multi-class metrics: micro- or macro-averaged precision, recall, and F1-score. (To learn more about multi-class metrics, check my Multi-Class Metrics Made Simple series, Part I and Part II; also, see my post on the kappa score, also known as Cohen’s kappa coefficient)" 
  
  "For binary classification, there is another (and arguably more elegant) solution: treat the true class and the predicted class as two (binary) variables, and compute their correlation coefficient (in a similar way to computing correlation coefficient between any two variables). The higher the correlation between true and predicted values, the better the prediction. This is the phi-coefficient (φ), rechristened Matthews Correlation Coefficient (MCC) when applied to classifiers."
  (https://towardsdatascience.com/the-best-classification-metric-youve-never-heard-of-the-matthews-correlation-coefficient-3bf50a2f3e9a)

[Matthews Correlation Coefficient (MCC)]()

Formula for MCC: https://en.wikipedia.org/wiki/Matthews_correlation_coefficient
    MCC = (TP * TN - FP * FN) / sqrt((TP + FP) * (TP + FN) * (TN + FP) * (TN + FN))
    



