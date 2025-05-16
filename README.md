# Cafe Chat Assistant

 This project is a **simple AI-powered chatbot** built using **Flask** and **vanilla JavaScript**.
 It uses a small neural network model trained on custom intents (defined in a JSON file), enabling the chatbot to understand and respond to user input.
 
---

## Features

* Trainable intent-based chatbot using PyTorch
* Web interface with JavaScript frontend
* Flask backend with RESTful API
* Customizable intents and responses

---

## Installation

1. **Clone the repository** and set up a virtual environment:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
python3 -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

2. **Install dependencies:**

```bash
pip install Flask torch torchvision nltk
```

3. **Download NLTK tokenizer model:**

```python
python
>>> import nltk
>>> nltk.download('punkt')
```

---

## Train the chatbot model

Update `intents.json` with your own tags, patterns, and responses. Then run:

```bash
python train.py
```

This creates a `data.pth` file that stores the trained model.

To test the chatbot in the terminal:

```bash
python chat.py
```

---

## Run the web app

Start the Flask app:

```bash
python app.py
```

Then open your browser and go to `http://127.0.0.1:5000/`.

---

## Project Structure

```
├── app.py              
├── app.js              
├── templates/
│   └── index.html      
├── static/
│   ├── style.css       
│   ├── app.js         
│   └── images/
│       └── chatbox-icon.svg
├── intents.json        # Chatbot intents (tags, patterns, responses)
├── model.py            # Neural network model
├── train.py            # Model training
├── data.pth            # Trained model weights
└── utils.py            # Helper functions
```

---


## Acknowledgments

* Frontend design inspiration: [hitchcliff/front-end-chatjs](https://github.com/hitchcliff/front-end-chatjs)
* Backend inspired by: [python-engineer/chatbot-deployment](https://github.com/python-engineer/chatbot-deployment)
