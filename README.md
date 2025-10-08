# legalEase


Legal  Chatbot
A chatbot for Rwandan legal knowledge in English, French, and Kinyarwanda using Sentence Transformers and FAISS.

Description
legalEase is a web platform designed to support rwandans and foreigner living in rwanda in accessing Rwandan penal code articles by equiping them with legal knowledge. It combines multilingual semantic search and an intelligent ChatBot to provide instant access to legal information.

The search component uses a fine-tuned multilingual Sentence Transformer model to analyze legal queries in English, French, or Kinyarwanda and find the most relevant legal articles. The system employs FAISS for efficient similarity matching and includes intent recognition to handle greetings, legal queries, and out-of-domain questions.

The Conversational ChatBot allows users to interactively ask legal questions, receive relevant article matches with similarity scores, and obtain multilingual legal guidance. This combination of semantic search and conversational chatbot makes legal information more accessible and user-friendly across different languages.

rwanda-legal-ai-assistant/
│
├── main.py                 # FastAPI application
├── enhanced_chatbot.py     # Chatbot with intent handling
├── requirements.txt        # Dependencies
├── run_api.py             # Production runner
├── test_api.py            # API testing script
│
├── fine-tuned-multilingual-legal-model/     # Trained model
├── multilingual_legal_articles.index        # FAISS search index
└── multilingual_article_info.pkl            # Article metadata
