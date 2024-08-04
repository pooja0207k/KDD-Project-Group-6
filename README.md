# Predictive Modeling of Health Risks Associated with Mobile Phone Usage

### Group Number: 6
#### Team Members:
1. Pooja Reddy Kadari
2. Phiny Francis Govathoti
3. Vedant Patel
4. Eswar Chand Vuppala

### Project Introduction 
This project will explore the impact of mobile phone usage on students' health. The dataset includes various attributes related to students' mobile phone habits and health symptoms. The primary goal of this diagnostic and predictive project is to understand the correlation between mobile phone usage and its effects on students' health. Using supervised learning, we aim to predict specific outcomes, such as health impact, based on input features like daily usage time and types of activities performed on mobile phones. Classification techniques will be employed to categorize the data into different impact levels, providing valuable insights into the relationship between mobile phone usage and student well-being. With this being said, this leads to our question that we will research.

### Research Question
How does the duration and type of mobile phone usage affect the health of young adults?

### Relevant Domain Information 
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9368281/#:~:text=Excessive%20mobile%20device%20usage%2C%20such,in%20weight%20in%20our%20study.

https://therapybrands.com/blog/what-is-the-impact-of-smartphone-addiction-on-mental-health/


#### Data Source: 
https://www.kaggle.com/datasets/innocentmfa/students-health-and-academic-performance


The dataset has the following attributes :
* Names: Student names
* Age	: Student age (in years)
* Gender : Male/Female	
* Mobile phone : Do students own a mobile phone? (Yes/No)
* Mobile Operating System : Type of mobile operating system used (e.g. Android, iOS, Other)	
* Mobile phone use for education : Do students use their mobile phone for educational purposes?(Sometime/ Frequently /Rarely )
* Mobile phone activities : List of mobile phone activities used for educational purposes (e.g. online research, educational apps, email, online learning platforms)
* Helpful for studying : Do students find mobile phone use helpful for studying? (Yes/No)	
* Educational Apps : List of educational apps used.	
* Daily usages : Average daily time spent using mobile phone for educational purposes (in hours)
* Performance impact: How does mobile phone use impact academic performance? (Agree/ Neutral/ Strongly agree)
* Usage distraction: Does mobile phone use distract from studying? (During Exams / Not Distracting / During Class Lectures / While Studying)	
* Attention span: Has mobile phone use affected attention span? (Yes / No)
* Useful features: What features of mobile phones are useful for learning? (e.g. Internet Access, Camera, Calculator, Notes Taking App)
* Health Risks: Are students aware of potential health risks associated with excessive mobile phone use? (Yes / No / Only Partially)
* Beneficial subject: Which subjects benefit most from mobile phone use? (e.g. Accounting, Browsing Material, Research)
* Usage symptoms: Are students experiencing any physical or mental symptoms related to mobile phone use? (e.g. Sleep disturbance, headaches, Anxiety or Stress, All of these)
* Symptom frequency: How often are symptoms experienced? (Sometimes / Never / Rarely / Frequently)
* Health precautions: Are students taking precautions to mitigate potential health risks? (Taking Break during prolonged use / Using Blue light filter / Limiting Screen Time / None of Above)
* Health rating: How would students rate their overall physical and mental health? (Excellent / Good / Fair / Poor)

### Understanding the Data
The dataset primarily includes students aged 21-25, with a mix of both genders, all of whom own mobile phones. It features students using both major mobile operating systems, Android and IOS. A significant number of students use their mobile phones for educational purposes with varying frequencies. Common activities on mobile phones include social media and multiple simultaneous activities. Many students report experiencing various health symptoms due to mobile phone usage, such as headaches and sleep disturbances, with some taking precautions like using blue light filters. Regarding academic impact, students have mixed perceptions, ranging from neutral to strongly agreeing on the negative impact of mobile phone usage. The daily usage time varies among students, with some using their phones for more than 6 hours daily.

### Data Preparation
* Initially, we retained essential columns, including `Health Risks`, `Mobile Phone`, `Age`, `Daily usages`, and `Health rating`. This subset was chosen based on relevance to the predictive task.
* Age ranges were converted to numerical midpoints for easier modeling. For instance, '16-20' was converted to 18, '21-25' to 23, and so on.
* We have encoded Categorical Variables. The `Health Risks` and `Mobile Phone` columns were mapped to numerical values, where 'No' became 0 and 'Yes' became 1.
* The `Daily usages` column was transformed into numerical values, with categories such as '< 2 hours' becoming 1 and '> 6 hours' becoming 4.
* Health ratings were encoded into numerical values, with ratings like 'Poor' mapped to 0 and 'Excellent' to 7.
* Rows with missing values were dropped to ensure that the dataset used for modeling was complete.
* Features (`X`) and target (`y`) variables were defined, with `Health Risks` as the target and the remaining columns as features.
* The features were scaled using MinMaxScaler to normalize the data between 0 and 1



### Collab Link 
https://colab.research.google.com/drive/1pAqfKaF0ZcYinfafGhFDIAqUP-5blAXI?usp=sharing 

## Modeling
Two primary modeling approaches were utilized:
**Traditional Models**:
   - Logistic Regression
   - Decision Tree Classifier
   - Random Forest Classifier
   - Support Vector Classifier (SVC)
   - K-Nearest Neighbors (KNN)
   - AdaBoost Classifier
   - Gradient Boosting Classifier
   - Stochastic Gradient Descent (SGD) Classifier
   - Gaussian Naive Bayes

2. **PyCaret**:
   - Setup and comparison of models.
   - Tuning and evaluation of the best model.

## Evaluation

- **Top Models**: KNN, SVC, AdaBoost with accuracy of 0.750.
- **Consistent Models**: Random Forest, Gradient Boosting, Gaussian Naive Bayes with accuracy of 0.700.
- **Underperformers**: SGD Classifier with accuracy of 0.250.

## Conclusion/Results

### Best Performers:
K-Nearest Neighbors (KNN), Logistic Regression Score, and AdaBoost Classifier all achieved the highest accuracy of 75%. These models also showed good performance in the classification reports with high precision and recall for class 1.0.

### Consistent Performers:
Random Forest, Gradient Boosting, and Gaussian Naive Bayes achieved an accuracy of 0.700. These models showed consistent performance with high recall for the positive class but struggled with precision and recall for the negative class (0.0).

### Underperformer:
SGD Classifier performed poorly with an accuracy of 0.250 and failed to effectively predict the positive class (1.0). It misclassified all instances of this class, indicating it may not be suitable for this dataset.

### Known Issues

Several issues were identified:

1. **Class Imbalance**: The dataset exhibited class imbalance, leading to low precision and recall for the negative class (`0.0`). This imbalance skewed performance metrics and made the models appear more effective than they were in practice.
   
2. **Model Bias**: There was evident bias towards the positive class (`1.0`), affecting the performance on the negative class. This bias highlights a skewed utility of the models when both classes are equally important.

3. **Accuracy Limitations**: Relying solely on accuracy was misleading due to class imbalance. Metrics such as precision, recall, and F1-score were crucial for a more accurate evaluation.

4. **Feature Engineering**: Current feature selection and engineering may not fully capture the underlying data patterns, potentially limiting model performance.

5. **Hyperparameter Tuning**: Models like Random Forest and Gradient Boosting would benefit from more thorough hyperparameter tuning to enhance their performance.

Addressing these issues through techniques like resampling, adjusting class weights, and refining feature engineering and hyperparameters is essential for improving model accuracy and generalization.

