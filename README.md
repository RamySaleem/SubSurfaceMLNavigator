# SubSurfaceMLNavigator
## Geological Inference Through Displacement-Distance Profile Guided by Machine Learning. 

![](https://i.imgur.com/OqN9F4J.jpg)

This research study offers a comprehensive exploration of the process involved in developing optimal machine learning (ML) models for predicting various key attributes of thrust structures along vertical sections within a coalmine dataset. Specifically, it focuses on predicting fault length, distance from a reference point (located at the upper tip of the fault), maximum displacement, and displacement-distance profile patterns. The methodology employed encompasses a series of steps, including the creation of ML models, feature selection, data partitioning, data exploration, training process optimization, performance assessment, and practical applications. A total of eight ML models, including linear regression, decision trees, random forests, lasso, ridge regression, elastic net, light GBM regressor, and extreme gradient boosting (XGBoost), were evaluated for predicting fault length, distance from a reference point, and maximum displacement using a dataset containing 110 faults and 930 samples, with five input features.

Additionally, five classification models, namely K nearest neighbour (KNN), decision trees, support vector machine (SVM), logistic regression, and random forests, were trained to classify displacement-distance profile patterns of the thrusts under investigation. To assess the robustness of these ML models, the dataset was divided into training, validation, and testing sets (comprising 90, 10, and 10 faults, respectively). The performance of these ML models was thoroughly evaluated, and the results were visually presented using histogram plots.

The outcomes of this study highlighted the four most reliable and accurate ML models for predicting various fault attributes. Notably, the Random Forest model emerged as the top performer, achieving an impressive accuracy in predicting fault length with R-squared values of 0.8832 and 0.8825, along with associated MAE values of 327 and 325, and RMSE values of 565 and 561 on the validation and testing sets, respectively. Additionally, the Decision Tree model excelled in predicting distance from the reference point, achieving R-squared values of 0.8890 and 0.9440, MAE values of 82 and 76, and RMSE values of 181 and 195 on the validation and testing sets, respectively.

For the task of estimating maximum displacement, the Random Forest model demonstrated strong predictive capabilities, yielding R-squared values of 0.9490 and 0.9172, MAE values of 27 and 74, and RMSE values of 50 and 145 on the validation and testing sets, respectively. In contrast, the Random Forest Classifier model exhibited exceptional performance in classifying displacement-distance profile patterns, achieving accuracy rates of 0.80 on both the validation and testing sets, precision rates of 0.82 and 0.70, and recall rates of 0.87 and 0.75, respectively.

Collectively, these four models offer a valuable tool for generating displacement-distance plots and subsurface fault conceptual models, providing interpretational guidance enriched with critical details such as lithology, reading locations on the fault, and uncertainty classification. This comprehensive workflow, incorporating regression and classification ML models, serves as an indispensable initial interpretation guide based on displacement-distance profiles.

Acknowledgements 
=================
This research presents findings derived from a PhD study conducted within the framework of the Natural Environment Research Council (NERC) Centre for Doctoral Training (CDT) in Oil & Gas. Funding for this study was generously provided, with 50% coming from NERC through its National Productivity Investment Fund (grant number NE/R01051X/1) and the remaining 50% granted by the University of Aberdeen via its PhD Scholarship Scheme. We express our sincere gratitude to both organisations for their unwavering support. Our research heavily relies on open-source Python libraries, particularly Pandas, Numpy, Seaborn, Plotly, and Matplotlib. We extend our appreciation to the developers and contributors of these libraries and to GitHub for their invaluable open-access hosting services, which make our Python scripts accessible to the broader research community.

![University of Aberdeen](https://i.imgur.com/PILyj4m.jpg)

![NERC-CDT](https://nerc-cdt-oil-and-gas.ac.uk/wp-content/uploads/news/2015-news-NERC-funding.jpg)

![NERC](https://auracdt.hull.ac.uk/wp-content/uploads/2019/11/UKRI_NER_Council-Logo_Horiz-RGB.png)

![CDT](https://i.imgur.com/QDOhcN3.png)
