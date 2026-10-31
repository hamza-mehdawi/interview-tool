# Interview Chatbot

A mock job interview app built with Streamlit and the Groq API. The user enters their background, chooses a position and a company, and answers interview questions from an AI "HR executive". At the end, the app gives a score from 1 to 10 and written feedback.

## Features

- Setup form: name, experience, and skills
- Choose the level (Junior, Mid-level, Senior)
- Choose the position (Data Scientist, Data Engineer, ML Engineer, BI Analyst, Financial Analyst)
- Choose the company (Amazon, Meta, Udemy, 365 Company, Nestle, LinkedIn, Spotify)
- Live chat with streaming answers from the AI interviewer
- The interview ends after 5 user answers
- "Get Feedback" button: overall score (1 to 10) and written feedback
- "Restart Interview" button to start again

## How It Works

1. **Setup stage:** the user fills in personal information and selects the level, position, and company.
2. **Interview stage:** the app sends a system prompt with this information to the Groq model. The model acts as an HR executive and interviews the user. Answers are streamed to the screen.
3. **Feedback stage:** after 5 answers, the full conversation is sent to the model again with a feedback prompt. The model returns a score and feedback.

## Tech Stack

- Python
- [Streamlit](https://streamlit.io/): web interface
- [Groq API](https://console.groq.com/): language model (`openai/gpt-oss-120b`)
- python-dotenv: loads the API key from a `.env` file
- streamlit-js-eval: used for the restart button

## Installation

1. Clone the repository:

```bash
git clone https://github.com/hamza-mehdawi/interview-tool.git
cd interview-tool
```

2. Install the requirements:

```bash
pip install -r requirements.txt
```

3. Create a file named `.env` in the project folder and add your Groq API key:

```
GROQ_API_KEY=your_groq_api_key_here
```

Get a key from the [Groq Console](https://console.groq.com/). The `.env` file is listed in `.gitignore`, so it is not uploaded to GitHub.

## Run the App

```bash
streamlit run "complete chat bot and feedback for interview.py"
```

The app opens in your browser at `http://localhost:8501`.

## Project Files

| File | Description |
|---|---|
| `complete chat bot and feedback for interview.py` | Main Streamlit app |
| `requirements.txt` | Python packages |
| `.gitignore` | Files that Git ignores (including `.env`) |

## Deploy Model
https://interview-tool-chatbot.streamlit.app/

