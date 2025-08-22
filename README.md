# University FAQ Chatbot (Console-based, PyTorch)

A simple **console-based chatbot** built with PyTorch.
It’s designed to answer **university admission FAQs**, but you can easily customize it for other use cases.

## Features

* Feed-forward neural network with 2 hidden layers
* Trains on intents and patterns defined in `intents.json`
* Lightweight, beginner-friendly, and easy to extend
* Runs entirely in the console (no web UI required)

## Project Structure

```
university-faq-chatbot/
│
├── chat.py          # Runs the chatbot (console interaction)
├── train.py         # Trains the model and saves it to data.pth
├── model.py         # Defines the neural network
├── nltk_utils.py    # Tokenization, stemming, and bag-of-words
├── intents.json     # Training data (questions and answers)
├── data.pth         # Saved model (after training)
├── README.md        # Project documentation
└── requirements.txt # (optional) Dependencies
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/SonaniAkshit/university-chatbot-console.git
cd university-chatbot-console
```

### 2. Create a virtual environment

```bash
python -m venv myenv
```

### 3. Activate the environment

Mac / Linux:

```bash
source myenv/bin/activate
```

Windows:

```bash
myenv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install torch nltk
```

OR

```bash
pip install -r requirements.txt
```

Download NLTK tokenizer data:

```bash
python
>>> import nltk
>>> nltk.download('punkt')
```

## Usage

### Train the model

```bash
python train.py
```

This will generate a `data.pth` file with the trained model.

### Start chatting

```bash
python chat.py
```

Type your question in the console. To quit, type:

```
quit
```

## Customization

Update [`intents.json`](intents.json) with your own **tags**, **patterns**, and **responses**.
For example:

```json
{
  "tag": "admission_deadline",
  "patterns": ["When is the admission deadline?", "Last date to apply?"],
  "responses": ["The admission deadline is July 15th."]
}
```

After editing `intents.json`, retrain:

```bash
python train.py
```

---

⭐ If you find this project useful, consider giving it a **star** on GitHub!
🍴 Feel free to **fork** it and adapt it for your own chatbot use case.

---