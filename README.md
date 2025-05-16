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
$ git clone https://github.com/Amir-Sa02/Cafe-Chat-Assistant
$ cd Cafe-Chat-Assistant
$ python -m venv venv
$ . venv/bin/activate  # On Windows use: venv\Scripts\activate
```

2. **Install dependencies:**

```bash
$ pip install Flask torch torchvision nltk
```

3. **Download NLTK tokenizer model:**

```python
$ (venv) python
>>> import nltk
>>> nltk.download('punkt')
>>> nltk.download('punkt_tab')
```

---

## Train the chatbot model

Optionally, you can update `intents.json` with your own tags, patterns, and responses. Then run:

```bash
$ (venv) python train.py
```
This creates a `data.pth` file that stores the trained model.

**Notice:**  The model is trained before and you can also use the chatbot without doing this part.

To test the chatbot in the terminal:

```bash
$ (venv) python chat.py
```

---

## Run the web app

Start the Flask app:

```bash
$ (venv) python app.py
```

Then open your browser and go to `http://127.0.0.1:5000/`.

---

## Acknowledgments

* Frontend design inspiration: [hitchcliff/front-end-chatjs](https://github.com/hitchcliff/front-end-chatjs)
* Backend inspired by: [python-engineer/chatbot-deployment](https://github.com/python-engineer/chatbot-deployment)
