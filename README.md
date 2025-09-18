# mlproject | Predict student performance

_Predict student performance based on study-related factors (study hours, test preparation, etc.) and uncover the key drivers of academic success._

---

# Table of Contents
<a href="#overview">Overview</a><br>
<a href="#dataset">Dataset</a><br>
<a href="#tools-technologies">Tools & Technologies</a><br>
<a href="#data-cleaning-preparation">Data cleaning & Preparation</a><br>
<a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a><br>
<a href="#Model-Selection">Model Selection</a><br>
<a href="#Model-Training-and-Evaluation">Model Training and Evaluation</a><br>
<a href="#Actual-vs-Predicted-table">Actual vs Predicted table</a><br>
<a href="#conclusion">Conclusion</a><br>
<a href="#author-contact">Author Contact</a><br>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>
Goal: Predict student performance using available features (parent education, test preparation, gender, etc.) and discover what drives scores.
This helps demonstrate how basic exam data can be used for insights and predictions in education

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

-CSV file located in data folder consisting thousands of rows.<br>

---
<h2><a class="anchor" id="tools-technologies"></a>Tool's and Technologies</h2>

-Python(Pandas, Matplotlib, Seaborn, Scipy)<br>
-scikit learn (ML)<br>
-GitHub

---
<h2><a class="anchor" id="data-cleaning-preparation"></a>Data cleaning & Preparation</h2>
-Converted data types, handled outliers
-Checked for the null values, duplicate values.


---
<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>
-Get to know which factors influence student performance.

**Feature Engineering**
-To enhance the analysis, two new columns were created: total_score and average, which represent the combined and average scores of the three subjects.

Key Findings and Insights
**Score Distribution:**
-Mean scores (math, reading, and writing) are very similar, ranging from 66 to 69. However, the minimum scores vary(math-0, writing-10, and reading-17).

**Performance:**
-Students performed best in reading (17 students) and worst in maths (7 students). 
Conversely, students who scored less than 20 in math (4 students) than in reading (1 student) or writing (3 students).

**Correlations:**
-The scores for math, reading, and writing are positively correlated and increase linearly with each other.


---
<h2><a class="anchor" id="Model-Selection"></a>Model Selection</h2>
Model Selection & Training

->Data Preparation
   -Prepared the data by separating the features (X) from the target variable (y), which is the math_score. 
   -The categorical features are then processed using OneHotEncoder, while the numerical features are scaled using StandardScaler. 
   -The data is then split into training and testing sets, with 80% for training and 20% for testing.

1. **Model Comparison:**
Nine different regression models were trained and evaluated on both the training and testing datasets.The models were compared based on their R2 Score on the test set.

Model Name              R2_Score
Ridge	                    0.880593
Linear Regression	        0.880433
AdaBoost Regressor	      0.852212
Random Forest Regressor 	0.851932
...                       ...

-Found Linear Regression worked best with 0.88 R2_score.

2.**Model Evaluation:**
-Measured accuracy using R², MAE, RMSE.

**Linear Regression**
 Model performance for Training set
- Root Mean Squared Error: 5.3231
- Mean Absolute Error: 4.2667
- R2 Score: 0.8743

Visualizations:

-Actual vs. Predicted Plot → Most points near diagonal = good predictions.
-Residuals Plot → Errors scattered randomly = unbiased model.


---
<h2><a class="anchor" id="Actual-vs-Predicted-table"></a>Actual vs Predicted table</h2>

**Created table with:**

-Actual score
-Predicted score
-Difference (error)


Actual_Value	Predicted_Value	      Difference

91	          76.387970	            14.612030
53	          58.885970	            -5.885970
80	          76.990265	             3.009735
74	          76.851804	            -2.851804
84	          87.627378	            -3.627378
...	...     	...	...
52	          43.409149	             8.590851
62	          62.152214	            -0.152214
74	          67.888395            	 6.111605
65	          67.022287	            -2.022287
61	          62.345132	            -1.345132


---
<h2><a class="anchor" id="conclusion"></a>Conclusion"</h2>

-Model Accuracy: Linear Regression predicted scores with 88.04% accuracy.

-Our analysis showed that math, reading, and writing scores are strongly correlated, and gender differences exist in subject-wise performance i.e. female students tended to excel in reading and writing, while male students performed slightly better in math.. 

**Value:**
      -This project highlights how educational institutions can leverage exam data to understand student strengths and weaknesses and design targeted interventions.
      -Schools can use this to identify at-risk students and provide timely help.

Future Work:
-Can Collect more features (attendance, sleep patterns, socio-economic factors).
-Try advanced models (Random Forest, Gradient Boosting).

---
<h><a class="anchor" id="author-contact"></a>Author Contact</h2>

**Simran Choudhary**
Data Analyst <br>
Email: choudharysimran235002@gmail.com <br>
[LinkedIn](https://www.linkedin.com/in/simran-choudhary-04a953299/) <br>
[Portfolio](https://portfoliosimran23.netlify.app/)