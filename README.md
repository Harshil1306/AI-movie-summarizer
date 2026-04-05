# 🎬 Movie Information Extractor

A simple AI-powered web app built with Streamlit and LangChain that extracts structured movie data from unstructured text using a large language model.

## 🚀 Features

- Convert plain movie descriptions into structured JSON
- Extract key details like:
  - Title
  - Release Year
  - Genre
  - Director
  - Cast
  - Rating
  - Summary
- Clean UI built with Streamlit
- Schema validation using Pydantic
- Robust parsing with LangChain output parsers

## 🛠️ Tech Stack

- Frontend/UI: Streamlit  
- LLM Integration: LangChain  
- Model Provider: Mistral AI  
- Schema Validation: Pydantic

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/movie-info-extractor.git
```
```bash
cd movie-info-extractor
```

### 2. Add Environment Variables

Create a `.env` file:

```bash
MISTRAL_API_KEY=your_api_key_here
```

## ▶️ Run the App

streamlit run UICore.py

## 🧠 How It Works

1. User enters a movie description.
2. A prompt is generated using LangChain’s ChatPromptTemplate.
3. The LLM processes the text and returns structured JSON.
4. PydanticOutputParser validates and parses the response.
5. The structured data is displayed in the UI.

## 📸 Example Input

Inception is a 2010 science fiction film directed by Christopher Nolan, starring Leonardo DiCaprio...

## 📸 Example Output

{
  "title": "Inception",
  "release_year": 2010,
  "genre": ["Science Fiction", "Thriller"],
  "director": "Christopher Nolan",
  "cast": ["Leonardo DiCaprio"],
  "rating": 8.8,
  "summary": "A thief enters dreams to steal secrets..."
}

## ⚠️ Error Handling

- Displays warning if input is empty
- Handles parsing errors when the model output doesn't match schema
- Shows raw model output for debugging

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.
