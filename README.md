

# Early Mental Health Prediction Using Machine Learning
# Author Name : Mounika Chinta
# Project Overview

This project develops a machine learning prototype for early mental
health prediction using structured survey data. The study compares
multiple classification models, applies hyperparameter optimisation,
evaluates predictive performance, and uses explainability techniques to
identify the factors influencing predictions. The final prototype
provides an interactive interface where users can enter relevant
parameters and receive a prediction.

Dataset

The project uses the Mental Health Dataset published on Kaggle by
Bhavikjikadara (2024).

Dataset source:
https://www.kaggle.com/datasets/bhavikjikadara/mental-health-dataset

The dataset contains demographic, behavioural, occupational, social, and
mental health-related variables. Important features used in the analysis
include family_history, care_options, Country, self_employed,
mental_health_interview, Gender, Days_Indoors, Growing_Stress,
Changes_Habits, Mood_Swings, Coping_Struggles, Work_Interest,
Social_Weakness, Mental_Health_History, and Occupation.

Machine Learning Models

Four machine learning classification models were evaluated:

Logistic Regression

Random Forest

CatBoost

Gradient Boosting

The models were first evaluated using baseline configurations.
Hyperparameter optimisation was then applied to improve selected model
settings and compare baseline and tuned performance.

Baseline Model Results

The baseline results showed clear differences between the four machine
learning models. Logistic Regression produced an F1-score of
approximately 0.6899. Random Forest achieved an F1-score of
approximately 0.8550 in the comparative performance analysis and
demonstrated strong overall classification capability. CatBoost achieved
strong performance across the evaluation metrics, while Gradient
Boosting also produced competitive results.

The baseline comparison demonstrated that ensemble-based approaches were
generally more effective than Logistic Regression for the dataset.
Random Forest showed particularly strong performance in the initial
evaluation, indicating that nonlinear relationships and feature
interactions were important for mental health prediction.

Tuned Model Results

Hyperparameter optimisation was applied to investigate whether model
performance could be improved. The F1-score comparison between baseline
and tuned models showed the following results:

Model                   Baseline F1-Score   Tuned F1-Score

Logistic Regression                0.6899           0.6900
Random Forest                      0.6950           0.7449
CatBoost                           0.7653           0.7784
Gradient Boosting                  0.7437           0.7748

The tuned results demonstrate that optimisation improved Random Forest,
CatBoost, and Gradient Boosting. CatBoost achieved the highest F1-score
of 0.7784 and was therefore identified as the best-performing model
based on the selected evaluation criterion.

Best Performing Model

CatBoost achieved the strongest final F1-score of 0.7784 after
hyperparameter optimisation. This result indicates an improved balance
between precision and recall compared with the other evaluated
configurations.

Gradient Boosting achieved a tuned F1-score of 0.7748 and performed
closely behind CatBoost. Random Forest improved substantially after
tuning and achieved 0.7449. Logistic Regression showed almost no
improvement, remaining close to 0.6900.

These results demonstrate the value of hyperparameter optimisation and
confirm that model selection should be based on comparative evaluation
rather than relying on a single baseline algorithm.

SHAP Explainability Results

SHAP analysis was used to provide global and local explanations of model
behaviour. The results consistently identified family_history as the
most influential feature. Other important features included
care_options, Country, Gender, mental_health_interview, and
self_employed.

The SHAP summary and mean absolute SHAP value results showed that
family_history had the largest influence on the model output. The local
explanation analysis also demonstrated how individual feature values
could increase or decrease predictions for specific test instances.

This analysis improved transparency by showing that the model was not
treated as a black box. Instead, the contribution of important features
could be examined at both global and individual levels.

LIME Explainability Results

LIME was used to explain individual predictions for multiple test
instances. The results showed that family_history repeatedly had a
strong influence on predictions across the analysed instances.

Other influential factors varied depending on the individual case and
included care_options, Country, self_employed, mental_health_interview,
Days_Indoors, Social_Weakness, Mood_Swings, and Occupation.

The LIME results complemented SHAP by providing case-specific
explanations. This demonstrated that the importance and direction of
individual features could change according to the characteristics of
each prediction instance.

Permutation Feature Importance Results

Permutation feature importance provided an additional model-agnostic
assessment of feature relevance. The highest-ranked features were:

family_history

care_options

Country

self_employed

mental_health_interview

Gender

The permutation importance results strongly supported the SHAP findings.
family_history and care_options were the two most influential features,
followed by Country. The remaining features had considerably lower
importance values.

The agreement between permutation importance and SHAP increased
confidence in the overall interpretation of the model.

Prototype Results

A functional desktop prototype was developed for early mental health
prediction. The interface allows users to select input values for
demographic, behavioural, occupational, and mental health-related
factors.

The prototype provides a prediction result and records prediction
history. It also includes Clear and Exit functions to support usability.
Different input combinations were successfully tested and produced
different prediction outcomes, including Treatment Required and No
Treatment Required.

The prototype demonstrates how the trained machine learning model can be
integrated into a practical and accessible application environment.

Human Evaluation

The prototype includes a structured human evaluation section covering
Ease of Use, Interface Design, Prediction Satisfaction, and Overall
Experience. Users can select evaluation responses and provide additional
comments.

The human evaluation component was included to assess the usability and
practical presentation of the prototype rather than evaluating machine
learning performance alone. This provides an additional perspective on
whether the system can be understood and used effectively by potential
users.

The inclusion of human evaluation supports the practical validation of
the developed prototype and complements the technical performance and
explainability results.

Key Findings

The experimental results demonstrate that machine learning can provide
useful predictive capability for the early identification of mental
health-related treatment requirements within the selected dataset.

CatBoost achieved the strongest tuned F1-score of 0.7784. Gradient
Boosting achieved 0.7748, while Random Forest improved to 0.7449 after
optimisation. Logistic Regression remained close to 0.6900.

The explainability analyses consistently identified family_history and
care_options as highly influential variables. The agreement between
SHAP, LIME, and permutation feature importance strengthened the
reliability of the interpretation.

The final prototype successfully integrated the predictive model into an
interactive application and demonstrated the practical applicability of
the research.

Technologies Used

Python

Pandas

NumPy

Scikit-learn

CatBoost

SHAP

LIME

Matplotlib

Tkinter

How to Run the Project

Install the required Python libraries.

Prepare the dataset and preprocessing pipeline.

Train or load the selected machine learning model.

Run the prototype application.

Enter the required input parameters.

Select Predict to generate the prediction result.

Use the Human Evaluation section to record usability feedback.

Project Structure

Data contains the dataset used for analysis.

Notebooks or Scripts contain preprocessing, model training,
optimisation, and evaluation code.

Models contains saved trained models.

Results contains performance results and visualisations.

Prototype contains the interactive application.

README.md provides project documentation.

Conclusion

The project demonstrates a complete machine learning workflow for early
mental health prediction, from data preparation and model comparison to
hyperparameter optimisation, explainability analysis, prototype
development, and human evaluation.

The results showed that CatBoost achieved the strongest final F1-score
of 0.7784. Explainability techniques consistently identified
family_history and care_options as major influential features. The final
prototype translated the technical model into an interactive system,
demonstrating the practical value of combining predictive modelling,
transparent interpretation, and user-focused evaluation
