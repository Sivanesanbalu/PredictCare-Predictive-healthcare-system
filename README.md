# 🤖 Disease Prediction AI – SymptoScan

A smart AI chatbot that helps users predict possible diseases based on symptoms entered in any format. This project uses NLP techniques to extract symptoms from natural language input, maps them to known conditions, and provides relevant health suggestions.

---

## 🚀 Features

- 🗣️ Accepts symptom input in conversational language (e.g., "I'm suffering from fever and sore throat").
- 🔍 Extracts and maps symptoms using regex + dictionary matching.
- 🧠 Predicts disease using a custom-trained model (plug your model via `get_predicted_value`).
- 🧾 Returns details including:
  - Description of the disease
  - Suggested medications
  - Precautionary steps
  - Workouts and diets
- 💬 Gradio-based chatbot interface

---

## 🔧 How It Works

1. **Input Parsing**:
   - Removes common phrases like "I have", "I feel".
   - Splits symptoms using `,`, `and`, `or`, etc.

2. **Symptom Mapping**:
   - Each normalized symptom is matched against a dictionary (`symptom_mapping`) to standardize inputs.

3. **Prediction**:
   - A pre-defined function (`get_predicted_value`) returns the most probable disease based on symptoms.

4. **Response Generation**:
   - Fetches detailed data using helper functions (like `helper(disease)`).
   - Returns a structured response with health guidance.

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| Python | Backend logic |
| Gradio | UI interface |
| Regex | Symptom parsing |
| Custom Model (placeholder) | Disease prediction |
| Dictionary Mapping | Symptom normalization |

---

Input:
  I’m suffering from dry cough, chest pain, and difficulty breathing.
Output:
  ================= Predicted Disease =============
Disease: Pneumonia

================= Description ==================
Pneumonia is an infection that inflames the air sacs...

================= Precautions ==================
1: Rest well
2: Avoid cold exposure
...

================= Medications ==================
1: Azithromycin
2: Paracetamol
...

================= Workouts ======================
1: Breathing exercises
...

================= Diets ==========================
1: Warm fluids
2: High-protein meals
...
