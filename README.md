# Smart CardioCare – Heart Disease Risk Prediction System

## Overview
<p>
Smart CardioCare is a web-based application that predicts the risk of heart disease using machine learning techniques based on user health data.

This project was originally based on an existing open-source implementation and has been **modified and enhanced** to meet specific project requirements.
</p>


---


## Aim

  To predict heart disease according to input parameter values provided by user and dataset
stored in database.


---

## Objective
<p>
  The main objective of this project is to develop a heart disease prediction system. The system
can discover and extract hidden knowledge associated with diseases from a historical heart data
set Heart disease prediction system aims to exploit data mining techniques on medical data set
to assist in the prediction of the heart diseases.
</p>

---

##  Key Features
- User input for health parameters  
- Heart disease risk prediction using ML model  
- Web-based interface built with Django  
- Data processing and analysis using Python  


---

## 📊 Model Performance
- Achieved **88.52% accuracy** on prediction model
  
---
## System Analysis
### Technology Used:
- #### Languages:
  - ![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
  - ![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
  - ![JAVASCRIPT](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
  - ![PYTHON](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=darkgreen)
- #### FrameWork:
  - ![BOOTSTRAP](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
  - ![DJANGO](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=green)
- #### Machine-Learning Algorithms:
  - <a href="https://en.wikipedia.org/wiki/Gradient_boosting">**GRADIENT BOOSTING ALGORITHM**</a>
  - <a href="https://en.wikipedia.org/wiki/Logistic_regression">**LOGISTIC REGRESSION**</a>
- #### ML/DL:
  - ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
  - ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
  - ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
- Database:
  - ![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
- #### Data-Set for training:
  - <a href="https://github.com/Mahix098/Smart_CardioCare/blob/main/Machine_Learning/heart.csv">Click here for DATA-SET</a>
- #### IDE:
  - ![VS Code](https://img.shields.io/badge/Visual_Studio_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white)
  - ![pyCharm](https://img.shields.io/badge/PyCharm-000000.svg?&style=for-the-badge&logo=PyCharm&logoColor=white)
- #### OS used for testing:
  - ![MacOS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=apple&logoColor=white)
  - ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
  - ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
    
---

### Modules:
- **Patient Login:-** *Patient Login to the system using his ID and Password.*
- **Patient Registration:_** *If Patient is a new user he will enter his personal details and he
will user Id and password through which he can login to the system.*
- **My Details:-** *Patient can view his personal details.*
- **Disease Prediction:-** *- Patient will specify the input parameter values. System will take
input values and predict the disease based on the input data values specified by the
patient and system will also suggest doctors based on the locality*
- **Search Doctor:-** *Patient can search for doctor by specifying name, address or type.*
- **Feedback:-** *Patient will give feedback this will be reported to the admin*
- **Doctor Login:-** *Doctor will access the system using his User ID and Password.*
- **Patient Details:-** *Doctor can view patient’s personal details.*
- **Notification:-** *Admin and doctor will get notification how many people had accessed
the system and what all are the diseases predicted by the system.*
- **Admin Login:-** *Admin can login to the system using his ID and Password.*
- **Add Doctor:-** *Admin can add new doctor details into the database.*
- **Add Dataset:-** *Admin can add dataset file in database.*
- **View Doctor:-** *Admin can view various Doctors along with their personal details.*
- **View Disease:-** *Admin can view various diseases details stored in database.*
- **View Patient:-** *Admin can view various patient details that had accessed the system.*
- **View Feedback:-** *Admin can view feedback provided by various users.*
  
---

## Model Training(Machine Learning)

```javascript
def prdict_heart_disease(list_data):
    csv_file = Admin_Helath_CSV.objects.get(id=1)
    df = pd.read_csv(csv_file.csv_file)

    X = df[['age','sex','cp','trestbps','chol','fbs','restecg','thalach','exang','oldpeak','slope','ca','thal']]
    y = df['target']
    X_train, X_test, y_train, y_test = train_test_split(X, y, train_size=0.8, random_state=0)
    nn_model = GradientBoostingClassifier(n_estimators=100,learning_rate=1.0,max_depth=1, random_state=0)
    nn_model.fit(X_train, y_train)
    pred = nn_model.predict([list_data])
    print("Neural Network Accuracy: {:.2f}%".format(nn_model.score(X_test, y_test) * 100))
    print("Prdicted Value is : ", format(pred))
    dataframe = str(df.head())
    return (nn_model.score(X_test, y_test) * 100),(pred)
```
### For a detailed Report <a href="https://github.com/Mahix098/Smart_CardioCare/blob/main/REPORT/SmartCardioCare_Report.pdf">Click Here</a>

---

## Output Screen-shots
When the application is runned then, a Welcome Page pops-up
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/banner.png" />

Admin Dash-board:
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/admin_dash.png" />

User Dash-board:
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/user_dash.png" />

Entering Heart Details to check our Health:
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/heart_detail_form1.png" />
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/heart_detail_form2.png" />

Prediction Result:
When the user is Healthy
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/healthy_predict1.png" />

<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/healthy_predict2.png" />

When the user's heart is at Risk
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/unhealthy_predict1.png" />
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/unhealthy_predict2.png" />

Since these details are stored in the Data-base, so we can also retrieve past results:
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/history.png" />

Doctor Dash-board:
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/doctor_dash.png" />

To view registered Doctor information:
<img src="https://github.com/Mahix098/Smart_CardioCare/blob/main/SCREENSHOTS/doctor_records.png" />

---
## ▶️ How to Run

1. Clone the repository
git clone https://github.com/Mahix098/SmartCardioCare.git

2. Install dependencies
pip install -r requirements.txt

3. Run the server
python manage.py runserver

4. Open in browser
http://127.0.0.1:8000/
