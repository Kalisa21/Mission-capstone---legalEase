# legalEase

## Description
LegalEase A chatbot for Rwandan legal knowledge in English, French, and Kinyarwanda using Sentence Transformers and FAISS.

Description 

legalEase is a web platform designed to support rwandans and foreigner living in rwanda in accessing Rwandan penal code articles by equiping them with legal knowledge. It combines multilingual semantic search and an intelligent ChatBot to provide instant access to legal information.

The search component uses a fine-tuned multilingual Sentence Transformer model to analyze legal queries in English, French, or Kinyarwanda and find the most relevant legal articles. The system employs FAISS for efficient similarity matching and includes intent recognition to handle greetings, legal queries, and out-of-domain questions.

The Conversational ChatBot allows users to interactively ask legal questions, receive relevant article matches with similarity scores, and obtain multilingual legal guidance. This combination of semantic search and conversational chatbot makes legal information more accessible and user-friendly across different languages.  

## GitHub Repository


## Project Structure
```

mission-capstone---legalEase/
│── Data/
│   ├── penal_sheet1.csv          
│
├─ README.md
├─ requirements.txt
├─ multilingual_article_info.pkl
├─ main.py
├─ fine-tuned-multilingual-legal-model
└─ legalEase.ipynb

````

scores 

| Query Language | Top-1 Accuracy | Top-5 Accuracy | Precision@5 | Recall@5 | F1-score@5 |
| -------------- | -------------- | -------------- | ----------- | -------- | ---------- |
| English        | 0.87           | 0.95           | 0.92        | 0.89     | 0.905      |
| French         | 0.84           | 0.93           | 0.91        | 0.87     | 0.89       |
| Kinyarwanda    | 0.80           | 0.90           | 0.88        | 0.85     | 0.865      |
| **Overall**    | 0.84           | 0.93           | 0.90        | 0.87     | 0.887      |

## Environment Setup
1. Clone the repository:
```bash
git clone https://github.com/yourusername/legalEase.git
cd legalEase
````

2. Create a virtual environment and activate it:

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## Running the Platform

Start the FastAPI app:

```bash
python -m uvicorn main:app --reload
```

Open your browser and go to:

```
http://127.0.0.1:8000
```

You can test the API endpoints via the **Swagger UI** available at:

```
http://127.0.0.1:8000/docs
```

## API Endpoints

* `GET /` – Returns a success message if the API is running.
* `POST /query` – Accepts citizen query in string format and returns the related articles.

### Example JSON for `/query`:

```json
{
  "query": "my husband is living with his concubine"
}
```

## Deployment Plan

The legalEase web platform will be deployed on [Render](https://render.com) for public access. Deployment includes:

1. Exposing FastAPI endpoints for the predictive model.
2. Using Swagger UI to demonstrate predictions.
3. Integrating the Conversational ChatBot for interactive guidance and explanations in the near future.
4. Expanding the platform to a complete web interface for patient input and prediction results display.

## Video Demo

[Click to Watch the Demo Video](https://www.youtube.com/watch?v=eSwuXgh3sZM)

The demo highlights:

* Running the FastAPI server
* Accessing the Swagger UI
* Making predictions with sample patient data
* Displaying predicted risk and confidence

## Notes

* This submission focuses on the initial software demo.
* The user interface is currently via **Swagger UI**, not a full web app.

```
