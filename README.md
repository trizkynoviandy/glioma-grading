# Glioma Grading with Ensemble Machine Learning

Glioma grading plays a crucial role in determining the appropriate treatment strategy for patients. Traditionally, glioma grading is performed by pathologists through manual examination of histopathological images. However, this process can be time-consuming, subjective, and prone to inter-observer variability. By leveraging machine learning, we can develop a more efficient and objective grading system.

## Dataset
In this project, we explore the use of machine learning algorithms to classify gliomas into different grades based on a tabular dataset obtained from the TCGA (The Cancer Genome Atlas). The dataset contains various features extracted from glioma samples, along with their corresponding grade labels. Dataset can be downloaded [here](https://archive-beta.ics.uci.edu/dataset/759/glioma+grading+clinical+and+mutation+features+dataset).

## Methodology

The proposed method involves the following steps:

**Data Preparation**: The TCGA tabular dataset is preprocessed and split into training and testing sets.

**Classifier Initialization**: Several machine learning classifiers, including Logistic Regression, Support Vector Machines (SVM), K-Nearest Neighbors (KNN), Random Forest, and AdaBoost, are initialized with their respective parameters.

**Voting Classifier Creation**: Different combinations of the initialized classifiers are used to create ensemble voting classifiers using soft voting.

**Model Evaluation**: The performance metrics, including accuracy, precision, recall, F1 score, and confusion matrix, are computed for each classifier.

## Results and Discussion

The performance of the glioma grading system using different voting classifiers is as follows:

| Classifier              | Accuracy | Precision | Recall | F1 Score |
|-------------------------|----------|-----------|--------|----------|
| lr, svm, knn            | 0.869    | 0.82      | 0.924  | 0.869    |
| lr, svm, rf             | 0.875    | 0.83      | 0.924  | 0.874    |
| lr, svm, adaboost       | 0.869    | 0.82      | 0.924  | 0.869    |
| lr, knn, rf             | 0.875    | 0.83      | 0.924  | 0.874    |
| lr, knn, adaboost       | 0.875    | 0.822     | 0.937  | 0.876    |
| lr, rf, adaboost        | 0.875    | 0.83      | 0.924  | 0.874    |
| svm, knn, rf            | 0.875    | 0.83      | 0.924  | 0.874    |
| svm, knn, adaboost      | 0.869    | 0.82      | 0.924  | 0.869    |
| svm, rf, adaboost       | 0.863    | 0.826     | 0.899  | 0.861    |
| knn, rf, adaboost       | 0.869    | 0.828     | 0.911  | 0.867    |
| lr, svm, knn, rf        | 0.875    | 0.83      | 0.924  | 0.874    |
| lr, svm, knn, adaboost  | 0.869    | 0.82      | 0.924  | 0.869    |
| lr, svm, rf, adaboost   | 0.875    | 0.83      | 0.924  | 0.874    |
| lr, knn, rf, adaboost   | 0.875    | 0.83      | 0.924  | 0.874    |
| svm, knn, rf, adaboost  | 0.875    | 0.83      | 0.924  | 0.874    |
| lr, svm, knn, rf, adaboost | 0.875 | 0.83      | 0.924  | 0.874    |


Based on the results obtained, it was observed that the performance metrics varied for different combinations of machine learning algorithms used in the glioma grading system. The following key findings can be highlighted:

* High accuracy scores, ranging from 0.863 to 0.875, were consistently achieved by the combinations of classifiers lr, svm, knn, rf, and adaboost. This indicates that the complex patterns present in the glioma dataset were effectively captured by the ensemble of these classifiers.

* The precision scores for most combinations were significant, with values ranging from 0.82 to 0.83. This implies that the classifiers performed well in correctly identifying positive instances of different glioma grades.

* The recall scores across the combinations were consistently high, with values around 0.924. This indicates that the classifiers exhibited a good ability to identify a high proportion of positive instances, minimizing the risk of false negatives.

* The F1 scores, which consider both precision and recall, were relatively high, ranging from 0.861 to 0.876. This suggests that the classifiers achieved a balanced trade-off between precision and recall in the glioma grading task.

Overall, the results demonstrate the potential of using ensemble voting classifiers with different combinations of machine learning algorithms for automating glioma grading. These findings contribute to the development of an efficient and objective system for assisting pathologists in accurate glioma classification.

## Conclusion

The results obtained from applying machine learning algorithms to glioma grading demonstrate promising potential for automating the grading process. The ensemble of classifiers, including lr, svm, knn, rf, and adaboost, achieves high accuracy, precision, recall, and F1 scores. This approach shows effectiveness in capturing complex patterns in the glioma dataset and can assist pathologists in making accurate grading decisions, leading to improved treatment outcomes. Further research can explore enhancements and practical implementations of this automated system.

## Related Works

Here are some relevant works related to glioma grading and machine learning:

* Ranjith et al. (2015). [Machine learning methods for the classification of gliomas: Initial results using features extracted from MR spectroscopy](https://journals.sagepub.com/doi/10.1177/1971400915576637). *The Neuroradiology Journal*.
* Tasci et al. (2022). [Hierarchical Voting-Based Feature Selection and Ensemble Learning Model Scheme for Glioma Grading with Clinical and Molecular Characteristics](https://www.mdpi.com/1422-0067/23/22/14155). *International Journal of Molecular Sciences*.