# Predicting Educational Performance Through Analysis of Mobile Phone Usage and Health Metrics

### Group Number: 6
#### Team Members:
1. Pooja Reddy Kadari
2. Phiny Francis Govathoti
3. Vedant Patel
4. Eswar Chand Vuppala

### Project Introduction 
This project will explore the impact of mobile phone usage on students' health. The dataset includes various attributes related to students' mobile phone habits, health symptoms, and academic perceptions. The primary goal of this diagnostic and predictive project is to understand the correlation between mobile phone usage and its effects on students' health and academic outcomes. Using supervised learning, we aim to predict specific outcomes, such as health impact and academic performance, based on input features like daily usage time and types of activities performed on mobile phones. Classification techniques will be employed to categorize the data into different impact levels, providing valuable insights into the relationship between mobile phone usage and student well-being. With this being said, this leads to our question that we will research.

### Research Question
How does the duration and type of mobile phone usage affect the health of young adults?

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

#### Project Objective:
The project focuses on analyzing mobile phone usage and health metrics to predict its impact on academic performance based on factors such as mobile phone activities, daily usage patterns, performance impact during exams, usage distraction, attention span, useful features utilized for education, health risks, beneficial subjects for mobile learning, symptoms related to mobile phone use, frequency of symptoms, health precautions taken, and students' self-rated health status.

### Understanding the Data
The dataset primarily includes students aged 21-25, with a mix of both genders, all of whom own mobile phones. It features students using both major mobile operating systems, Android and IOS. A significant number of students use their mobile phones for educational purposes with varying frequencies. Common activities on mobile phones include social media and multiple simultaneous activities. Many students report experiencing various health symptoms due to mobile phone usage, such as headaches and sleep disturbances, with some taking precautions like using blue light filters. Regarding academic impact, students have mixed perceptions, ranging from neutral to strongly agreeing on the negative impact of mobile phone usage. The daily usage time varies among students, with some using their phones for more than 6 hours daily.

### Data Preparation
Currently, the dataset has undergone several data preparation steps to ensure its quality and suitability for analysis. Initially, the dataset contained some missing values in columns like 'Mobile phone use for education', 'Mobile phone activities', and 'Helpful for studying', which were addressed by dropping the affected rows. Categorical data, such as age ranges and daily usage time, were converted to numerical values by mapping age ranges to their midpoints and assigning numerical values to usage categories. Categorical variables like 'Gender', 'Mobile Operating System', 'Mobile phone activities', and 'Educational Apps' were transformed using one-hot encoding to facilitate analysis. Additionally, numerical columns like 'Age' and 'Daily usage' were normalized to have a mean of 0 and a standard deviation of 1, ensuring that the data was standardized and ready for further analysis.
