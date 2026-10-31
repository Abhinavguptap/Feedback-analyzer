# AI Customer Feedback Analyzer

An AI-powered customer feedback analysis application built with Python, FastAPI, Streamlit, and Google Gemini. It helps analyze customer reviews, identify sentiment, assign ratings, and extract key feedback themes.

## Features

- **AI Sentiment Analysis:** Classifies reviews as positive, negative, or neutral.
- **Customer Rating:** Generates a sentiment score from 1 to 5.
- **Theme Extraction:** Identifies the main topic of each review.
- **REST API:** Provides review analysis through FastAPI.
- **Interactive Interface:** Uses Streamlit for submitting and viewing feedback.
- **Review Storage:** Uses SQLite to store feedback analysis history.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| FastAPI | REST API development |
| Google Gemini API | AI-powered review analysis |
| Pydantic | Data validation and structured responses |
| Streamlit | User interface |
| SQLite | Local database |

## Project Structure

```text
project/
├── api.py
├── app.py
├── database.py
├── src/
├── pyproject.toml
├── uv.lock
├── README.md
├── .gitignore
└── config.env.txt   # Local only; never upload
```

## Installation

**1. Clone the repository**

```bash
git clone https://github.com/Abhinavguptap/Feedback-analyzer.git
cd Feedback-analyzer
```

**2. Install dependencies**

Install `uv` if necessary, then run:

```bash
uv sync
```

**3. Configure your Gemini API key**

Create a file named `config.env.txt` in the project root:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Keep this file private and excluded from Git.

## Running the Application

Start the FastAPI backend:

```bash
uv run uvicorn api:app --reload
```

In another terminal, launch the Streamlit interface:

```bash
uv run streamlit run app.py
```

Open the local Streamlit URL displayed in your terminal.

## How It Works

1. A user submits a customer review.
2. The backend sends the review to Google Gemini for analysis.
3. Gemini returns structured sentiment, rating, and theme information.
4. The application displays the results and can store them in SQLite for review history.

## Future Improvements

- Batch analysis of customer reviews
- CSV upload and export
- Sentiment trends and analytics
- Cloud deployment
- User authentication
- Support for multiple languages

## Security

- API keys are stored in local environment configuration files.
- Secret files and local databases are excluded using `.gitignore`.
- API keys must never be committed to GitHub.

## Author

**Abhinav Gupta**

[GitHub](https://github.com/Abhinavguptap)
