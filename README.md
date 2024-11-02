# HealthWatch at TechCorp

## Project Overview
This project involves building a NLP and a CV model to generate diagnostics for patient using HealthWatch. The primary objective is to develop a model that can accurately classify illnesses according to their corresponding descriptions and to combine it with vizual input to confirm a diagnosis..

## Data Source
The dataset used for this project was obtained from 9 different sources, all from huggingface:
* ashnaz/fine_tuned_symptoms
* ashnaz/symptoms_diagnose_doctors_data
* akhileshav8/json_symptom
* celikmus/symptom_text_to_disease_01
* venetis/symptom_text_to_disease_mk3
* celikmus/mayo_clinic_symptoms_and_diseases_v1
* ninaa510/diagnosis-text
* venetis/symptom_text_to_disease_mk4
* gretelai/symptom_to_diagnosis

After well processing the dataset and augmenting it, it contains a description and its classification, and I later added a label for each category so that the model can process it.

## NLP
1. **Model Selection**:
   - Used the 'bert-base-uncased' model which is a transformer capable of understanding context.

2. **Model Training**:
   - Encapsulated training in a class and used some chosen configurations to train the model on a small training and testing set that is 10% the size of the original one.

3. **Evaluation Metrics**:
   - Accuracy was chosen as the primary metric because we had more than one class.


## Computer Vision
1. **Model Selection**:
   - Used the 'MTCNN' model which is a CV model pre-trained on detecting faces.

2. **Model Training**:
   - Manual tuning on videos of the written detection methods until I got satisfactory results.


## Key Insights
1. **Strengths**:
   - The model shows high precision in classification.

2. **Weaknesses**:
   - Has some bias towards hypertension.
   - CV sometimes wrongly detecs some signs because it needs to operate in perfect conditions.


## Conclusion
The model developed in this project provides a reliable tool for diagnosing illnesses and for basic diagnostics.

## Additional information

### Adversities during preparation
- Finding a Pre-Trained CV model
- Google Colab GPU limit
- Training a transformer model

### How to run the project
- Open the ipynb file in Google Colab
- Adjust the locations of the files in all the cells according to your drive
- Connect to your MongoDB database
- Run the cells in the order they're put in
