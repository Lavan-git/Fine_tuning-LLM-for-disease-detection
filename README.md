# 🚑 Disease Prediction Using Fine-Tuned LLM  
*A Machine Learning Project by Lavan Gupta*

---

## 📌 **Project Overview**

This project implements a complete workflow for **disease prediction** using a **fine-tuned Large Language Model (LLM)**.  
Given a set of symptoms, the model predicts the most likely disease and provides a short explanation and disclaimer.

The full pipeline includes:

- Dataset exploration and cleaning  
- Symptom & precaution preprocessing  
- JSONL dataset creation for instruction tuning  
- Fine-tuning an LLM (Gemma-2B) using LoRA  
- Prediction generation and parsing  
- Model evaluation using a confusion matrix  
- Three demo test-case predictions  
- Export and preparation of all required artifacts  

---

## 📂 **Repository Structure**

```
train.jsonl
test.jsonl
confusion_matrix.png
demo_outputs.json
preds_demo.json
assignment_artifacts.zip
Notebook.ipynb
README.md
```

---

## 📊 **Dataset Description**

### DiseaseAndSymptoms.csv  
- Contains Disease and 17 symptom columns  
- Many symptoms are missing → handled in preprocessing  

### Disease precaution.csv  
- Contains 4 precaution fields per disease  
- Merged into one combined text field  

---

## 🛠 **Preprocessing Steps**

- Lowercase + clean text  
- Merge all symptom columns into one string  
- Merge all precaution columns into one string  
- Merge symptoms + precautions on 'Disease'  
- Convert into JSONL instruction format  
- Split into train/test  

---

## 🤖 **Model: Gemma-2B (Fine-Tuned Using LoRA)**

Gemma-2B is small, efficient, and suitable for fine-tuning on Colab.  
LoRA enables parameter-efficient training on GPUs by modifying only a small number of model weights.

---

## 📈 **Evaluation**

A confusion matrix is generated comparing predicted vs actual diseases.  
Saved as:

```
confusion_matrix.png
```

---

## 🧪 **Demo Test Cases**

Three symptom inputs were tested:

1. `Symptoms: Fever, headache, body pain`  
2. `Symptoms: Fever, cough, sore throat`  
3. `Symptoms: itching, skin rash, nodal skin eruptions`  

Outputs stored in:

```
demo_outputs.json
```

---

## 📝 **Generated Files**

- train.jsonl  
- test.jsonl  
- confusion_matrix.png  
- demo_outputs.json  
- preds_demo.json  
- assignment_artifacts.zip  

---

## ▶️ **How to Run**

1. Open the Notebook in Google Colab  
2. Upload the two CSV files  
3. Run all cells in order  
4. Fine-tuned model will generate predictions + evaluation  

---

## 🙌 **Author**
**Lavan Gupta**
