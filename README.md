# SubSurfaceMLNavigator
Geological Inference Through Displacement-Distance Profile Guided by Machine Learning. 

This research study offers a comprehensive exploration of the process involved in developing optimal machine learning (ML) models for predicting various key attributes of thrust structures along vertical sections within a coalmine dataset. Specifically, it focuses on predicting fault length, distance from a reference point (located at the upper tip of the fault), maximum displacement, and displacement-distance profile patterns. The methodology employed encompasses a series of steps, including the creation of ML models, feature selection, data partitioning, data exploration, training process optimization, performance assessment, and practical applications. A total of eight ML models, including linear regression, decision trees, random forests, lasso, ridge regression, elastic net, light GBM regressor, and extreme gradient boosting (XGBoost), were evaluated for predicting fault length, distance from a reference point, and maximum displacement using a dataset containing 110 faults and 930 samples, with five input features.

Additionally, five classification models, namely K nearest neighbour (KNN), decision trees, support vector machine (SVM), logistic regression, and random forests, were trained to classify displacement-distance profile patterns of the thrusts under investigation. To assess the robustness of these ML models, the dataset was divided into training, validation, and testing sets (comprising 90, 10, and 10 faults, respectively). The performance of these ML models was thoroughly evaluated, and the results were visually presented using histogram plots.

The outcomes of this study highlighted the four most reliable and accurate ML models for predicting various fault attributes. Notably, the Random Forest model emerged as the top performer, achieving an impressive accuracy in predicting fault length with R-squared values of 0.8832 and 0.8825, along with associated MAE values of 327 and 325, and RMSE values of 565 and 561 on the validation and testing sets, respectively. Additionally, the Decision Tree model excelled in predicting distance from the reference point, achieving R-squared values of 0.8890 and 0.9440, MAE values of 82 and 76, and RMSE values of 181 and 195 on the validation and testing sets, respectively.

For the task of estimating maximum displacement, the Random Forest model demonstrated strong predictive capabilities, yielding R-squared values of 0.9490 and 0.9172, MAE values of 27 and 74, and RMSE values of 50 and 145 on the validation and testing sets, respectively. In contrast, the Random Forest Classifier model exhibited exceptional performance in classifying displacement-distance profile patterns, achieving accuracy rates of 0.80 on both the validation and testing sets, precision rates of 0.82 and 0.70, and recall rates of 0.87 and 0.75, respectively.

Collectively, these four models offer a valuable tool for generating displacement-distance plots and subsurface fault conceptual models, providing interpretational guidance enriched with critical details such as lithology, reading locations on the fault, and uncertainty classification. This comprehensive workflow, incorporating regression and classification ML models, serves as an indispensable initial interpretation guide based on displacement-distance profiles.

# Abstract
This study explores the development of effective machine-learning models to predict fault characteristics in coal mines. Using a dataset of 110 faults and 930 samples, eight regression models and five classification models were tested. The best-performing models, including Random Forest and Decision Tree, demonstrated high accuracy in predicting fault attributes. The study emphasizes the practical application of these models in creating displacement-distance plots and subsurface fault conceptual models, aiding interpretation with details like lithology and reading location on the fault. Overall, the workflow serves as a valuable first-step interpretation guide for displacement-distance profiles.

# Methodology

The workflow consists of six well-defined stages designed to address the complexities of subsurface interpretation. Here's a breakdown of the methodology:

1. **Fault Length Prediction:** Select an optimal regression model trained to predict fault length using various input features like vertical displacement, coal bed horizon name, lithological attributes, stratigraphic disposition, and horizon uncertainty.

2. **Distance Prediction:** Choose a regression model to predict distances from a reference point (upper tip of the fault). The predicted distance is stored for later use in predicting displacement-distance plots.

3. **Maximum Displacement Prediction:** Use the predicted fault length from the first step to estimate maximum displacement. Select a suitable regression model for this projection, setting the stage for displacement profile pattern predictions.

4. **Profile Pattern Prediction:** Establish an optimal classification model for predicting displacement-distance profile patterns. Inputs include fault length prediction and maximum displacement from previous steps.

5. **Integrative Model Outputs:** Combine predicted displacement-distance profile patterns to create a conceptual representation. Highlight stratigraphic offsets and convey mechanical stratigraphy attributes.

6. **Enhanced Subsurface Interpretation:** Utilize user input displacement values, predicted distances, fault length, maximum displacement, and profile patterns to generate a displacement-distance plot. This comprehensive guide aids interpreters in understanding complex geological systems and advancing subsurface structure comprehension.

# Machine Learning Model Performance:

## Correlation Analysis and Feature Importance:

In this study, a correlation matrix indicates strong relationships among input features, with notable correlations between total fault length and displacement-distance patterns (0.77) and between fault length and maximum displacement (0.76). Feature importance analysis identifies displacement and fault position as crucial, suggesting their significant impact on predictions. To address potential issues like overfitting, the study carefully selects input variables for each model.

## Evaluation of Model Performance:

Eight regression models and five classification models are assessed using validation and testing sets, ensuring robustness and generalization. The Random Forest model emerges as the most powerful predictor, achieving high accuracy in fault length (R-squared 0.8832), maximum displacement (R-squared 0.9490), and displacement-distance profile patterns (Accuracy 0.80) on the validation set. However, caution is advised due to potential overfitting in the Decision Tree model. Testing set results reaffirm model reliability, showcasing precision in predicting fault length (R-squared 0.8825), maximum displacement (R-squared 0.9172), and displacement-distance patterns (Accuracy 0.80). The models demonstrate promising applications across diverse coalmine datasets, underlining their reliability for subsurface predictions.

Future work
===========
To develop a workflow and web-based front end for the script, which will allow to interpret complete geological data.

Acknowledgements 
=================
The work contained in this repositories contains work conducted during a PhD study undertaken as part of the Natural Environment Research Council (NERC) Centre for Doctoral Training (CDT) in Oil & Gas funded 50% through its National Productivity Investment Fund grant number NE/R01051X/1 and 50% by the University of Aberdeen through its PhD Scholarship Scheme. The support of both organisations is gratefully acknowledged. The work is reliant on Open-Source Python Libraries, particularly numpy, OpenCV, cv2 matplotlib, bruges and pandas and contributors to these are thanked, along with Jovian and GitHub for open access hosting of the Python scripts for the study.

![University of Aberdeen](https://i.imgur.com/PILyj4m.jpg)

![NERC-CDT](https://nerc-cdt-oil-and-gas.ac.uk/wp-content/uploads/news/2015-news-NERC-funding.jpg)

![NERC](https://auracdt.hull.ac.uk/wp-content/uploads/2019/11/UKRI_NER_Council-Logo_Horiz-RGB.png)

![CDT](https://i.imgur.com/QDOhcN3.png)
