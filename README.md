# Creating-an-AI-Powered-Chatbot-for-Customer-Support-using-Natural-Language-Processing
The project is designed for beginner to intermediate ML learners and is an excellent demonstration of real-world customer service automation using NLP.

This project implements an AI-powered chatbot designed to assist customers by understanding their queries and responding intelligently using Natural Language Processing (NLP) techniques. The chatbot uses an intent classification model built with Python, scikit-learn, NLTK, and TF-IDF, making it lightweight, fast, and easy to deploy.

# Features

1. Intent Classification using Logistic Regression Preprocessing: tokenization, stopword removal, stemming
2. Predefined responses mapped to predicted intents
3. Customizable intents.json dataset
4. TF-IDF vectorization for text representation
5. Interactive chatbot interface (CLI + Gradio UI)
6. Easy to extend with more intents or LLM fallback

# project

│── intents.json         # Training dataset

│── model.pkl            # Trained ML model

│── train.py             # Model training script

│── chatbot.py           # Chatbot runtime script

│── README.md            # Documentation


How It Works
1. User Input:- The user enters a message like: "Where is my order?"

2. Preprocessing:- The text is cleaned using: lowercasing, tokenization, stopword removal, stemming

3. Vectorization:- The processed text is transformed using TF-IDF.

4. Intent Prediction:- A trained Logistic Regression model predicts an intent from categories like: greeting, order_status, refund_policy, complaint, thanks, goodbye

5. Response Generation:- A random response from the matching intent is selected and displayed.

# Technologies Used
1. Python
2. NLTK — text preprocessing
3. Scikit-learn — ML model + pipeline
4. TF-IDF Vectorizer
5. Logistic Regression
6. Joblib — model saving
7. Gradio (optional UI)

# TF-IDF Vectorizer:- 
It’s basically a text-to-numbers converter and it  only understands numbers.
Your chatbot can’t understand raw English like
“Where is my order?”

--> TF-IDF does this:
-- It takes every word
-- Checks how often the word appears
-- Checks how important the word is compared to other sentences
-- Converts the whole sentence into a vector of numbers (a list of values)
--This vector is what the ML model uses to detect the correct intent. So in short:TF-IDF is a method to convert sentences into meaningful numerical features.

 # Joblib —
 Model Saving:- Once you train a machine learning model, you don’t want to retrain it every time you chat with the bot.

Joblib allows you to:

Save the trained model to a file

Load it instantly anytime

Reuse it in other scripts

Like putting your trained model into a safe box (model.pkl) so you can open it later without training again.

💡 In short:
Joblib stores your ML model on disk so you can reuse it.

# Gradio (optional UI):-  
Gradio creates a simple web interface for your chatbot, so instead of typing into Python console, you get a cute little chatbox on a webpage.
| Tool                  | Simple meaning                | Why you need it                      |
| --------------------- | ----------------------------- | ------------------------------------ |
| **TF-IDF Vectorizer** | Converts text → numbers       | Helps model understand user messages |
| **Joblib**            | Saves and loads trained model | So you don’t retrain every time      |
| **Gradio**            | Makes a small web UI          | For clean chatbot interface          |


Example Interactions:-
1. User: hi
Bot: Hello! How can I help you today?

2. User: where is my order
Bot: Can you please provide your order ID? I can check the status.

3. User: I want a refund
Bot: You can return items within 30 days. Do you want me to create a return request?

# Future Enhancements

1. Add more intents and training data
2. Add a database for order lookup
3. Integrate with APIs
4. Add LLM fallback for unknown queries
5. Deploy as a web service (Flask / FastAPI)
6. Use a deep learning model (LSTM/BERT) for higher accuracy



    # Author
Madhumitha

AI Enthusiast

