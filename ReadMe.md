## **H1N1 AND SEASONAL FLU VACCINES**

Author: [Wallace Ouma](https://github.com/WKalawi)

![banner](https://github.com/WKalawi/H1N1-and-Seasonal-Flu-Vaccines/blob/main/Images/H1N1-VaccineEDIT.jpg)

## Business and Data Understanding

Data Source: [DrivenData](https://www.drivendata.org/competitions/66/flu-shot-learning/)

This project focuses on vaccination, a crucial public health strategy against infectious diseases, providing individuals with immunization and contributing to "herd immunity" when sufficiently prevalent within a community. While vaccines for COVID-19 are still in development at the time of this competition's launch, we will instead examine the public health response to a recent significant respiratory disease pandemic. Originating in spring 2009, the H1N1 influenza virus, commonly known as "swine flu," rapidly spread worldwide, causing a pandemic. Estimates suggest this virus led to between 151,000 to 575,000 deaths globally within its first year. A vaccine for H1N1 became available to the public in October 2009. Concurrently, the United States conducted the National 2009 H1N1 Flu Survey in late 2009 and early 2010, a phone survey querying respondents about their H1N1 and seasonal flu vaccine uptake alongside various personal details. These included social, economic, and demographic backgrounds, perceptions regarding illness and vaccine efficacy risks, and behaviors related to transmission prevention. Understanding how these factors interrelate with individual vaccination behavior can offer valuable insights for future public health strategies.

In this evaluation, the target variable pertains to whether an individual will voluntarily receive either an influenza or H1N1 vaccine, as indicated by past data randomly gathered from households across the United States. This data collection was conducted through random-digit-dialing of telephones within these households. Two distinct target variables exist: one for the H1N1 vaccine and another for the Seasonal Flu vaccine. These target variables are already clearly defined and binary, simplifying the preprocessing process. Given that the dataset is comprehensive, this evaluation will be approached as a supervised learning experience.

## Data Preparation

The dataset provided for addressing this issue is succinct and directly relevant to the business problem at hand. Both the testing and training data are formatted as feature vectors, facilitating modeling efforts with minimal need for extensive formatting adjustments. While some preprocessing steps are necessary, the dataset requires relatively little modification before processing. It encompasses responses from a telephone-administered survey, covering a range of topics including concerns and knowledge about H1N1, behavioral patterns like antiviral medication usage and social habits, recommendations from doctors regarding vaccines, presence of chronic medical conditions, and demographic details such as age, education, race, income, and employment status. During the data preparation phase, careful examination was undertaken for any missing values that could affect model evaluation, with replacement by mode values as appropriate. Additionally, identification and removal of outlier data points that could skew results were performed. Given that the survey was conducted randomly across the United States, the collected data and predicted outcomes should theoretically provide an accurate representation of the broader U.S. population.

## Modelling

The objective of developing a model using this data is to determine the probability of people who meet specific demographic parameters receiving either an H1N1 or seasonal influenza vaccination. This project will use a supervised learning method due to the comprehensive nature of the dataset. The dataset mainly comprises binary or numeric qualitative category factors and non-numeric demographic data from survey replies.

The dataset consists mainly of categorical data, with numeric values representing qualitative variables derived from survey replies rather than quantitative metrics. Several modeling strategies were investigated, such as logistic regression, gradient boosting classifier, decision tree, improved decision tree, random forest, optimized random forest, k-nearest neighbors, and ensemble modeling. The analysis was conducted using Python at Google Colaboratory. The assumption was that ensemble modeling, combining numerous models to build a more accurate and complete model, would provide the most optimal outcomes. The models chosen for integration into the ensemble model were based on their success rates, specifically focusing on the Area Under the Curve (AUC). Next, the models will be assessed by using them on the test dataset to compare their performance.

## Evaluation and Deployment

The effectiveness of models developed in this process will be determined by comparing their Area Under the Curve (AUC) values, a metric derived from the Receiver Operating Characteristic (ROC) curve. While accuracy is often used to gauge model performance, AUC offers a more insightful measure by considering the true positive rate against the false positive rate (Hozanoet al., 2017). This approach discourages the selection of models merely representative of data but not necessarily discriminative, thereby promoting models that achieve above-random chance true positive and false positive rates. By splitting the dataset into training and test sets, model performance can be accurately assessed. For each scenario, such as predicting H1N1 or seasonal flu vaccine recipients, separate training and test sets were created, allowing for rigorous evaluation. Feature scaling, which normalizes data for easier modeling, and Lasso (L1-Regularization) for feature selection were applied to enhance model robustness. The choice between models like Random Forest with Cross Validation and Gradient Boosting Classifier was informed by their performance and computational efficiency, considering resource constraints.

The primary objective of this modeling endeavor is cost reduction, particularly in mass vaccine production. By accurately predicting vaccine demand, organizations like the National Center for Immunization and Respiratory Diseases (NCIRD), National Center for Health Statistics (NCHS), and Centers for Disease Control and Prevention (CDC) can optimize resource allocation, mitigating unnecessary expenses. Furthermore, the model's insights could enable targeted outreach to individuals misinformed about vaccine risks, fostering better public health education and awareness. However, it's crucial to recognize that while this data-driven approach offers valuable predictive capabilities, it may not fully resolve the complexities of vaccine production challenges. External factors like the COVID-19 pandemic, which profoundly influences public attitudes towards vaccination, underscore the need for ongoing adaptation and refinement of modeling strategies. Despite the potential of these models to identify vaccine recipients, inherent limitations persist. The dataset, collected in 2009, may not fully capture contemporary attitudes and behaviors, especially in light of significant events like the COVID-19 pandemic. While the models provide valuable insights, they do not account for all factors influencing vaccine uptake. Nonetheless, by leveraging these predictive capabilities alongside broader public health strategies, organizations can make informed decisions to optimize vaccine distribution and combat infectious diseases effectively.

## Conclusion

The analysis of predictive models for H1N1 Vaccine and Seasonal Flu Vaccine acceptance reveals valuable insights into public health challenges. By utilizing past immunization survey data and various supervised learning algorithms, we assessed vaccine acceptance likelihood based on demographics. While ensemble modeling initially seemed promising, individual models often outperformed, raising concerns about overfitting. The Decision Tree (original) model excelled for H1N1 Vaccine prediction, while the Random Forest (CV) model showed superior performance for Seasonal Flu Vaccine prediction. These findings highlight the importance of tailored modeling techniques and the potential of predictive analytics to inform public health decisions. However, external factors like the COVID-19 pandemic may influence vaccine acceptance rates, necessitating ongoing model refinement. Overall, predictive modeling offers opportunities to optimize resource allocation, mitigate costs, and enhance intervention strategies for improved public health outcomes.


**Repository Components**

* `ReadMe`
* `ProjectNotebook`
* [`Presentation`](https://www.canva.com/design/DAF_Fwz82xM/7FGEg3AGxyPqvaodjZ65xQ/edit?utm_content=DAF_Fwz82xM&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
* `DataSets Directory`

**References**

DrivenData. (n.d.). Flu Shot Learning: Predict H1N1 and Seasonal Flu Vaccines. Retrieved March 4, 2024, from https://www.drivendata.org/competitions/66/flu-shot-learning/ 

Hozano, M., Antunes, N., Fonseca, B., & Costa, E. (2017). Evaluating the accuracy of machine learning algorithms on detecting code smells for different developers. Proceedings of the 19th International Conference on Enterprise Information Systems. https://doi.org/10.5220/0006338804740482

