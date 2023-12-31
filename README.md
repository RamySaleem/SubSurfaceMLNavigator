# SubSurfaceMLNavigator
## Geological Inference Through Displacement-Distance Profile Guided by Machine Learning. 

![](https://i.imgur.com/OqN9F4J.jpg)

This research study offers a comprehensive exploration of the process involved in developing optimal machine learning (ML) models for predicting various key attributes of thrust structures along vertical sections within a coalmine dataset. Specifically, it focuses on predicting fault length, distance from a reference point (located at the upper tip of the fault), maximum displacement, and displacement-distance profile patterns. The methodology employed encompasses a series of steps, including the creation of ML models, feature selection, data partitioning, data exploration, training process optimization, performance assessment, and practical applications. A total of eight ML models, including linear regression, decision trees, random forests, lasso, ridge regression, elastic net, light GBM regressor, and extreme gradient boosting (XGBoost), were evaluated for predicting fault length, distance from a reference point, and maximum displacement using a dataset containing 110 faults and 930 samples, with five input features.

Additionally, five classification models, namely K nearest neighbour (KNN), decision trees, support vector machine (SVM), logistic regression, and random forests, were trained to classify displacement-distance profile patterns of the thrusts under investigation. To assess the robustness of these ML models, the dataset was divided into training, validation, and testing sets (comprising 90, 10, and 10 faults, respectively). The performance of these ML models was thoroughly evaluated, and the results were visually presented using histogram plots.

The outcomes of this study highlighted the four most reliable and accurate ML models for predicting various fault attributes. Notably, the Random Forest model emerged as the top performer, achieving an impressive accuracy in predicting fault length with R-squared values of 0.8832 and 0.8825, along with associated MAE values of 327 and 325, and RMSE values of 565 and 561 on the validation and testing sets, respectively. Additionally, the Decision Tree model excelled in predicting distance from the reference point, achieving R-squared values of 0.8890 and 0.9440, MAE values of 82 and 76, and RMSE values of 181 and 195 on the validation and testing sets, respectively.

For the task of estimating maximum displacement, the Random Forest model demonstrated strong predictive capabilities, yielding R-squared values of 0.9490 and 0.9172, MAE values of 27 and 74, and RMSE values of 50 and 145 on the validation and testing sets, respectively. In contrast, the Random Forest Classifier model exhibited exceptional performance in classifying displacement-distance profile patterns, achieving accuracy rates of 0.80 on both the validation and testing sets, precision rates of 0.82 and 0.70, and recall rates of 0.87 and 0.75, respectively.

Collectively, these four models offer a valuable tool for generating displacement-distance plots and subsurface fault conceptual models, providing interpretational guidance enriched with critical details such as lithology, reading locations on the fault, and uncertainty classification. This comprehensive workflow, incorporating regression and classification ML models, serves as an indispensable initial interpretation guide based on displacement-distance profiles.

![](https://i.imgur.com/nz40m61.jpg)

# Abstract
This study explores the development of effective machine-learning models to predict fault characteristics in coal mines. Using a dataset of 110 faults and 930 samples, eight regression models and five classification models were tested. The best-performing models, including Random Forest and Decision Tree, demonstrated high accuracy in predicting fault attributes. The study emphasizes the practical application of these models in creating displacement-distance plots and subsurface fault conceptual models, aiding interpretation with details like lithology and reading location on the fault. Overall, the workflow serves as a valuable first-step interpretation guide for displacement-distance profiles.

# Dataset Overview:

## 1. Data Background:

The study area covers approximately 323.29 km² of closely spaced coal mines, reaching depths of up to 2 km. Data sources include mine workings, boreholes, seismic profiles, and surface exposures. Original interpretations by Drozdzewski et al. (1980) provided geological insights, forming the basis for a refined uncertainty classification framework. The structured dataset includes lithology, formation names, coal seams, and stratigraphic units.

## 2. Data Preparation:

The dataset consists of 14 subsurface cross-sections, focusing on the western region of the Ruhr coalfield. Analysis involved 346 traced thrust faults, with in-depth examination of 100 faults for training and validation sets and 10 for testing. Selection prioritized faults with calculable coal seam horizon displacement, enabling precise displacement-distance profile characterization.

## 3 Data Preprocessing:

Preprocessing involved splitting the dataset into training, validation, and testing sets, ensuring similarity between training and validation sets. Standard scaling was applied for normalization, transforming input features to a mean of 0 and standard deviation of 1.

## 4 Exploratory Data Analysis (EDA):

EDA included analysis of 930 data samples from 110 thrust faults, exploring both categorical and numerical data. Input features for ML models were identified, and histograms revealed insights into fault characteristics, spatial distribution, and geological parameters. Descriptive statistics, such as mean distance and displacement values, provided a comprehensive overview of the dataset, forming a foundation for further specialized analyses and ML modeling for fold-thrust structures.

![]([https://imgur.com/yQSFY4P](https://i.imgur.com/yQSFY4P.jpg))

# Methodology

The workflow consists of six well-defined stages designed to address the complexities of subsurface interpretation. Here's a breakdown of the methodology:

1. **Fault Length Prediction:** Select an optimal regression model trained to predict fault length using various input features like vertical displacement, coal bed horizon name, lithological attributes, stratigraphic disposition, and horizon uncertainty.

2. **Distance Prediction:** Choose a regression model to predict distances from a reference point (upper tip of the fault). The predicted distance is stored for later use in predicting displacement-distance plots.

3. **Maximum Displacement Prediction:** Use the predicted fault length from the first step to estimate maximum displacement. Select a suitable regression model for this projection, setting the stage for displacement profile pattern predictions.

4. **Profile Pattern Prediction:** Establish an optimal classification model for predicting displacement-distance profile patterns. Inputs include fault length prediction and maximum displacement from previous steps.

5. **Integrative Model Outputs:** Combine predicted displacement-distance profile patterns to create a conceptual representation. Highlight stratigraphic offsets and convey mechanical stratigraphy attributes.

6. **Enhanced Subsurface Interpretation:** Utilize user input displacement values, predicted distances, fault length, maximum displacement, and profile patterns to generate a displacement-distance plot. This comprehensive guide aids interpreters in understanding complex geological systems and advancing subsurface structure comprehension.

![](https://i.imgur.com/ScpIbFz.jpg)

![](https://i.imgur.com/rwWIoHO.jpg)

# Machine Learning Model Performance:

## Correlation Analysis and Feature Importance:

In this study, a correlation matrix indicates strong relationships among input features, with notable correlations between total fault length and displacement-distance patterns (0.77) and between fault length and maximum displacement (0.76). Feature importance analysis identifies displacement and fault position as crucial, suggesting their significant impact on predictions. To address potential issues like overfitting, the study carefully selects input variables for each model.

## Evaluation of Model Performance:

Eight regression models and five classification models are assessed using validation and testing sets, ensuring robustness and generalization. The Random Forest model emerges as the most powerful predictor, achieving high accuracy in fault length (R-squared 0.8832), maximum displacement (R-squared 0.9490), and displacement-distance profile patterns (Accuracy 0.80) on the validation set. However, caution is advised due to potential overfitting in the Decision Tree model. Testing set results reaffirm model reliability, showcasing precision in predicting fault length (R-squared 0.8825), maximum displacement (R-squared 0.9172), and displacement-distance patterns (Accuracy 0.80). The models demonstrate promising applications across diverse coalmine datasets, underlining their reliability for subsurface predictions.

![](https://i.imgur.com/syGMMLn.jpg)

# Conclusion:

This study extensively explored the effectiveness of machine learning (ML) models in predicting fault attributes, including length, distance from a reference point, maximum displacement, and displacement-distance profile patterns. Key findings and conclusions are summarized as follows:

- **Model Selection:** After evaluating eight ML models, Random Forest emerged as the most reliable for predicting fault length and maximum displacement, as well as classifying displacement-distance patterns. The Decision Tree model also demonstrated high reliability in predicting distances from a reference point.

- **Critical Input Features:** The study identified a set of five key input features crucial for accurate predictions, emphasizing their significance in achieving high precision for fault length and distance predictions. Any substantial reduction in input features resulted in decreased prediction accuracy.

- **Dataset Splitting Importance:** Effective dataset splitting into training, validation, and testing sets was highlighted as critical. Random splitting significantly impacted prediction performance, reinforcing the importance of careful data splitting based on geological, structural, or tectonic regions to ensure model stability and reliability.

- **Fault Attributes Analysis:** Geometric parameters, uncertainty classification, stratigraphic characteristics, and sample positioning were identified as major factors guiding subsurface interpretation using displacement-distance profiles.

- **Integration of ML Models:** The study advocated for the integration of regression and classification ML models as a comprehensive solution to complex subsurface interpretation challenges, addressing limitations inherent in standalone ML models.

In conclusion, this research showcased the significant potential and efficiency of ML techniques in guiding subsurface interpretations, providing a coherent workflow for predicting displacement-distance plots and associated subsurface fault conceptual models.

![](https://i.imgur.com/GnCfOfG.jpg)

![](https://i.imgur.com/ISA4Z2h.jpg)

Future work
===========
## Future Research Directions:

This research opens avenues for further exploration. Firstly, evaluating deep learning techniques like artificial neural networks could enhance fault attribute and displacement-distance profile predictions. Integrating these networks into a comprehensive framework may unveil their collective potential in addressing subsurface interpretation challenges.

Additionally, expanding data sources to include geological and geophysical data, such as seismic attributes or well-log information, could enhance model accuracy and robustness. This expansion may lead to a more thorough understanding and interpretation of subsurface faults.

Exploring the applicability of these models across diverse geological settings and regions is crucial to assess their adaptability and generalizability. Lastly, future studies could focus on developing predictive uncertainty quantification techniques to refine model interpretations, fostering the continuous integration of advanced techniques into practical subsurface exploration and environmental management activities.

![](https://i.imgur.com/iBbv2wU.gif)

Acknowledgements 
=================
This research presents findings derived from a PhD study conducted within the framework of the Natural Environment Research Council (NERC) Centre for Doctoral Training (CDT) in Oil & Gas. Funding for this study was generously provided, with 50% coming from NERC through its National Productivity Investment Fund (grant number NE/R01051X/1) and the remaining 50% granted by the University of Aberdeen via its PhD Scholarship Scheme. We express our sincere gratitude to both organisations for their unwavering support. Our research heavily relies on open-source Python libraries, particularly Pandas, Numpy, Seaborn, Plotly, and Matplotlib. We extend our appreciation to the developers and contributors of these libraries and to GitHub for their invaluable open-access hosting services, which make our Python scripts accessible to the broader research community.

![University of Aberdeen](https://i.imgur.com/PILyj4m.jpg)

![NERC-CDT](https://nerc-cdt-oil-and-gas.ac.uk/wp-content/uploads/news/2015-news-NERC-funding.jpg)

![NERC](https://auracdt.hull.ac.uk/wp-content/uploads/2019/11/UKRI_NER_Council-Logo_Horiz-RGB.png)

![CDT](https://i.imgur.com/QDOhcN3.png)
