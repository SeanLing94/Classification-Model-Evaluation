# Classification-Model-Evaluation
This section illustrates the important performance measures for evaluating the classification models' performance with categorical target attributes.

Three main approaches are available to test a classification model's quality:

Confusion matrices

ROC (Receiver Operator Characteristic) Curves and AUC

Lift charts. 

The following sub-sections show the concept of these approaches and the measures involved. 

The Confusion Matrix is the best approach used for evaluating Classification model performance. Understanding the confusion matrix requires comprehension of several definitions. Nevertheless, before presenting the definitions, we must examine a fundamental confusion matrix for a binary classification where there can be two labels (for example, Y or N). We assume Y represents the positive response of the classification problem to identify, and N is the negative response. The accuracy of a model classification can be one of four possible cases:

The predicted label is Y, and the actual label is Y → this is a correct prediction of a positive response. Therefore, it is a "True Positive" or TP.

The predicted label is Y, and the actual label is N → this is an incorrect prediction of a positive response. Therefore, it is a "False Positive" or FP.

The predicted label is N, and the actual label is Y → this is an incorrect prediction of a negative response. Therefore, it is a "False Negative" or FN.

The predicted label is N, and the actual label is also N → this is a correct prediction of a Negative response. Therefore, it is a "True Negative" or TN.

A fundamental confusion matrix is a 2 x 2 matrix structure, as in Table 1. The predicted labels may be arranged horizontally in rows, and the actual classes are arranged vertically in columns, although sometimes this order is reversed.

                                                          

We will now use these four possible cases to introduce commonly used terms for understanding and interpreting classification performance. For example, a perfect classifier will have no prediction for FP and FN. In other words, the number of FP = FN = 0.

The following explains the commonly used terms:

Sensitivity is the ability of a classifier to select all the positive response cases that need to be selected. A perfect classifier will select all the actual Y's and will not miss any actual Y's; conversely, it will have no false negatives. In reality, any classifier will miss some true Y's and thus have some false negatives. Sensitivity is a ratio (or percentage) computed as follows: TP/(TP + FN). However, sensitivity alone is not sufficient to evaluate a classifier. 

Precision is the proportion of cases found that were actually relevant. For example, suppose we run a specific term search, and that search returns 100 documents. Only 70 were relevant to the search. Furthermore, the search missed out on an additional 40 documents that could have been useful. For this example, the relevant number was 70; thus, the precision is 70/100 or 70%. The 70 documents were TP, whereas the remaining 30 were FP. Therefore precision is TP/(TP+FP).

Recall is the proportion of the relevant cases that were actually found among all the relevant cases. There are two types of recall, i.e., recall positive or recall negative. Using the example mentioned earlier, only 70 of the total 110 (i.e., 70 found + 40 missed) relevant cases (i.e., positive) were actually found, thus delivering a recall positive of 70/110 = 63.63%. Recall positive is also called Sensitivity, whereas Recall negative is called Specificity. Recall by default is known as sensitivity if we observe a recall measure without stating whether it is for a positive or negative response. We can see that recall positive is the same as sensitivity, computed as TP/(TP+FN).

Specificity is the ability of a classifier to reject all the negative cases that need to be rejected. A perfect classifier will reject all the actual N's and not yield unexpected results. In other words, it will have no false positives. However, in reality, any classifier will select some cases that need to be rejected and thus have some false positives. Specificity is a ratio (or percentage) computed as TN/(TN+FP).

Accuracy is the ability of the classifier to select all positive and negative response cases that need to be selected and all cases that need to be rejected. For example, for a classifier with 100% accuracy, this would imply that FN = FP = 0. Note that we have not indicated the TN in the document search example, as this could be large. Thus, Accuracy is (TP+TN)/(TP+FP+TN+FN). 

Finally, Misclassification is the complement of Accuracy, measured by (1 – Accuracy).

Precision and recall can be condensed into a single performance measure known as the F1. 


Fortunately, data mining practitioners do not need to memorize these equations because the data tools always automate the calculation according to the equations. However, having a sound fundamental understanding of these terms is essential.
