# 🩺 Health Prediction System Using Machine Learning

**A Python-based health prediction application developed using Random Forest Machine Learning and Tkinter.**

## About the Project

The Health Prediction System is a machine learning project I developed to explore how artificial intelligence and data science can be applied to healthcare. The main idea behind this project was to understand how different health indicators can be analyzed together to identify patterns associated with potential health risks.

Using Python and the **Random Forest Classification algorithm**, the system examines health-related parameters such as age, gender, blood pressure, cholesterol levels, heart rate, respiratory rate, blood sugar, and allergies. Based on the patterns learned from the training dataset, the model classifies the entered health information into two categories: Healthy or Unhealthy.

While developing this project, I wanted to go beyond simply training a machine learning model. I also designed an interactive graphical user interface using Tkinter, making it easier for users to enter their health information and view predictions without interacting directly with Python code.

This project allowed me to gain practical experience in data preprocessing, supervised machine learning, model development, and graphical interface design while exploring the possibilities and limitations of AI in healthcare.

**This application has been developed strictly for educational purposes and is not intended for medical diagnosis.**

---

## Project Status

**Version 1.0 — Functional Educational Prototype**

The project currently consists of a working machine learning classification model integrated with a desktop-based graphical interface.

The following components have been implemented:

- **Dataset Preparation:** Cleaning and organizing healthcare data, handling missing values, and converting categorical information into numerical representations.
- **Model Development:** Training a Random Forest Classifier using an 80:20 training-testing split.
- **Graphical User Interface:** Creating a Tkinter-based application with separate sections for patient information, allergies, and predictions.
- **Health Parameter Selection:** Implementing dropdown menus that allow users to select different ranges for their health measurements.
- **Prediction System:** Generating health classifications using the trained model alongside experimental rule-based adjustments.
- **Visual Feedback:** Displaying results through a color-coded interface, making the classifications easier to understand.

The current version demonstrates how a machine learning model can be integrated into a user-friendly application. However, the system is still an educational prototype, and further testing and validation would be necessary before considering any real-world healthcare applications.

---
## Application Screenshots

The following screenshots demonstrate the graphical interface and key features of the Health Prediction System.

### 1. Patient Details

The main interface allows users to enter patient information, including age, gender, blood pressure, cholesterol, heart rate, respiratory rate, and blood sugar levels.

![Patient Details](images/patient_details.png)

### 2. Allergy Selection

Users can select relevant allergies, including dust, nuts, pollen, and latex, or indicate that they have no known allergies.ho

![Allergy Selection](images/allergies_details.png)

### 3. Prediction Interface

The prediction tab allows users to analyze the entered health indicators using the machine learning model.

![Prediction Interface](images/prediction_portal.png)

### 4. Input Validation

The application displays a warning when required information is missing or an invalid value is entered.

![Input Validation](images/no_result.png)

### 5. Healthy Prediction

When the model predicts a healthy status, the result is displayed in green for easy identification.

![Healthy Prediction](images/correctly_predicted.png)

### 6. Unhealthy Prediction

When the model predicts an unhealthy status, the result is highlighted in red to indicate potential health concerns.

![Unhealthy Prediction](images/unhealthy_prediction.png)
---

## Key Features

### 1. Machine Learning-Based Health Prediction

The system uses a Random Forest Classifier, a supervised machine learning algorithm that combines multiple decision trees to identify patterns in data.

By analyzing the relationships between different health indicators and their recorded classifications, the model generates predictions for new inputs.

### 2. Analysis of Multiple Health Indicators

The application considers several parameters rather than relying on a single measurement.

These include:

- Age and gender
- Systolic and diastolic blood pressure
- Cholesterol levels
- Heart rate
- Respiratory rate
- Blood sugar levels
- Allergies

Together, these parameters form the input features used by the classification model.

### 3. Interactive Graphical User Interface

The application features a Tkinter-based graphical interface designed to simplify user interaction.

It contains three main sections:

**Patient Details:** Users enter their age and gender and select ranges for different health measurements.

**Allergies:** Users can select applicable allergies, including dust, nuts, pollen, and latex.

**Prediction:** The application processes the entered information and displays the predicted classification.

### 4. Color-Coded Prediction Results

The application displays its results using different colors:

- **Green:** Healthy classification
- **Red:** Unhealthy classification
- **Yellow:** Invalid input or processing error

This makes the output easier to interpret while keeping the interface simple.

### 5. Automated Data Preprocessing

The system uses Pandas and Scikit-learn to prepare the dataset before training.

This includes removing incomplete records, separating blood pressure measurements, encoding categorical variables, and organizing input features into a structured format.

---

## How It Works

The project follows a machine learning workflow that transforms raw healthcare data into predictions through several stages.

### Step 1: Loading and Preparing the Dataset

The program begins by loading a CSV dataset containing health-related measurements and their corresponding health classifications.

Using Pandas, the data is cleaned and organized. Missing values are removed, column names are standardized, and blood pressure readings are separated into systolic and diastolic values.

Categorical variables such as gender and allergies are then converted into numerical features using Label Encoding and One-Hot Encoding.

This ensures that the dataset is compatible with the machine learning algorithm.

### Step 2: Splitting the Dataset

After preprocessing, the dataset is divided into two parts:

| Dataset | Percentage | Purpose |
|---|---|---|
| Training Data | 80% | Used to train the classification model |
| Testing Data | 20% | Reserved for evaluating the model |

The training dataset helps the model identify patterns, while the testing dataset can be used to evaluate how well the model performs on previously unseen records.

### Step 3: Training the Random Forest Model

The project uses the Random Forest Classification algorithm from Scikit-learn.

Random Forest works by creating multiple decision trees, each learning relationships between the health parameters and their corresponding classifications.

The predictions of these trees are combined to produce a final classification.

This approach allows the model to capture relationships between several input variables without relying on a single decision tree.

### Step 4: Collecting User Information

Once the model has been trained, users can interact with the Tkinter application.

The interface allows them to enter their age, select their gender, choose predefined ranges for health measurements, and indicate any allergies.

Selected numerical ranges are converted into representative values before being passed to the model. For example, selecting a blood pressure range of 120–140 produces a midpoint value of 130.

### Step 5: Generating the Prediction

The application organizes the entered information into a Pandas DataFrame that matches the structure of the training dataset.

The trained Random Forest model then estimates the probability of each health classification.

The current implementation also includes experimental custom rules that adjust the classification in certain situations, including when allergies are selected.

These additional rules are part of the prototype and have not been medically validated.

### Step 6: Displaying the Results

Finally, the application displays the predicted health status through the Tkinter interface.

The result appears as either Healthy or Unhealthy, accompanied by color-coded visual feedback.

The output represents the classification generated by the application's model and rules, rather than a confirmed medical assessment.

---

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Dataset cleaning and manipulation |
| Scikit-learn | Machine learning implementation |
| Random Forest | Supervised classification |
| LabelEncoder | Encoding categorical information |
| Tkinter | Graphical user interface |
| Pillow | Image and logo handling |
| Jupyter Notebook | Development and execution |

---

## Installation and Usage

**1. Download or clone the repository.**

**2. Install the required Python libraries:**

`pip install -r requirements.txt`

**3. Ensure the dataset is available.**

Place `Save yourself.csv` in the same directory as the notebook.

**4. Open the Jupyter Notebook.**

Launch `health_prediction.ipynb` using Jupyter Notebook on a computer with a desktop graphical environment.

**5. Run the application.**

Execute the notebook to train the Random Forest model and launch the Tkinter interface.

**6. Enter the health parameters.**

Complete the patient details, select any allergies, and click **Predict Health Status** to generate a classification.

**Note:** Since the application uses Tkinter, it requires a graphical desktop environment and generally cannot display its interface directly in Google Colab.

---

## Future Improvements

Although the current version demonstrates the basic functionality of the system, several improvements could make the project more advanced and reliable.

- **Improved Model Accuracy:** Explore larger and more diverse datasets and experiment with additional machine learning algorithms.
- **Advanced Model Evaluation:** Implement cross-validation and evaluate performance using accuracy, precision, recall, and F1-score.
- **Web-Based Application:** Develop an accessible browser-based interface using Streamlit or Flask.
- **Better Data Handling:** Improve the processing of multiple allergies and introduce stronger input validation.
- **User Interface Improvements:** Introduce a more modern design with clearer visualizations and additional interactive features.

---

## Limitations and Educational Disclaimer

**FOR EDUCATIONAL PURPOSES ONLY**

This project was created to demonstrate how machine learning and predictive analytics can be applied to healthcare-related data.

The model has not undergone clinical validation, and its predictions depend on the quality and representativeness of the training dataset. Some classification adjustments are experimental and do not represent established medical risk calculations.

The application is not intended to diagnose, treat, prevent, or rule out any medical condition. Its results should not be used as a substitute for professional medical advice.

---

## License

This project is licensed under the **MIT License**, allowing others to use, modify, and distribute the source code in accordance with the license terms.

See the [LICENSE](LICENSE) file for further details.

## Contact

For questions, suggestions, feedback, or contributions related to the project, feel free to open an issue through this GitHub repository.

---

