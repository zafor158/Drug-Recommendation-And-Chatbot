# Drug-Recommendation-And-Chatbot
# 💊 AI-Driven Drug Recommendation & Chatbot System  
*Using Retrieval-Augmented Generation (RAG) and Fine-tuned LLMs*  

## 📖 Overview  
This project implements an **AI-powered drug recommendation system** and **medical chatbot** using **Retrieval-Augmented Generation (RAG)** combined with fine-tuned **Google Gemma** and **RoBERTaConvNet** models.  

It leverages **drug reviews, conditions, and official medical literature** to provide **personalized drug suggestions** and **accurate responses to medical queries**. The system is designed to support **patients** and **healthcare professionals** in making informed decisions.  

---

## ✨ Key Features  
- ✅ **Drug Recommendation Engine**: Predicts drug ratings based on reviews, side effects, conditions, and patient profiles.  
- 🤖 **Medical Chatbot**: Fine-tuned Gemma model + RAG for evidence-based answers.  
- 📊 **Data Sources**: [Drugs.com](https://www.drugs.com/), [UCI ML Drug Review Dataset](https://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset), [CDC](https://www.cdc.gov/).  
- 🔎 **Retrieval-Augmented Generation (RAG)**: FAISS-based vector search integrated with LangChain.  
- 📈 **High Accuracy Models**:  
  - RoBERTaConvNet: **90.21% accuracy** (RMSE 0.49).  
  - Gemma-2.0-7b: Fine-tuned with **Val Loss 0.0946**.  
- 🎨 **User-Friendly Interface**: Chat UI for patients & doctors.  

---

## 🏗️ System Architecture  
### 🔹 Data Layer  
- Drug information (name, class, dosage, warnings, side effects).  
- Patient reviews (200K+ from UCI dataset).  
- Disease-symptom mappings from CDC & Stanford SNAP.  

### 🔹 Model Layer  
- **RoBERTaConvNet** → Drug rating prediction.  
- **Gemma-2.0-7b (Fine-tuned)** → Context-aware responses.  

### 🔹 Retrieval Layer  
- Vector database (FAISS).  
- RAG pipeline for contextual search + response generation.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/394d836d-4873-434d-840a-187432732733" width="500"/>
</p>

---

## 📊 Results  
| Model              | RMSE   | Val Loss | R²     | Accuracy |
|--------------------|--------|----------|--------|----------|
| **RoBERTaConvNet** | 0.4907 | 0.4238   | 0.6741 | **90.21%** |
| NeuralNet V1       | 2.5547 | 6.6489   | 0.3561 | 71.61%   |
| XGBoost Optuna V1  | 2.3554 | 0.2531   | 0.2531 | 73.94%   |
| LightGBM Tuned     | 2.0456 | 2.0456   | 0.5895 | 77.28%   |
| BERT Seq Review    | 1.5013 | 0.9010   | 0.7789 | 83.32%   |

- **Human Evaluation (Avg. Scores)**:  
  - Relevance: 3.82  
  - Coherence: 3.66  
  - Fluency: 3.63  
  - Accuracy: 3.64  
  - Creativity: 3.55  

---

## 🖥️ User Interface  

<p align="center">
  <img  src="https://github.com/user-attachments/assets/18925427-310a-43ad-8585-4967c816a680" />

</p>  

---

## ⚙️ Installation & Usage  

```bash
# Clone repo
git clone https://github.com/your-username/drug-recommendation-chatbot.git
cd drug-recommendation-chatbot

# Create virtual environment
python -m venv venv
source venv/bin/activate   # For Linux/Mac
venv\Scripts\activate      # For Windows

# Install dependencies
pip install -r requirements.txt
