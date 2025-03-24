

### ** README.md**  

```md
# News Summarization & Sentiment Analysis App  

This repository contains a **News Summarization and Sentiment Analysis Application** that extracts news articles related to a company, analyzes sentiment, performs a comparative analysis, and generates a text-to-speech (TTS) output in Hindi. The application uses **FastAPI for the backend** and **Streamlit for the frontend**.

---

## 1. Features  
- Extracts **at least 10 news articles** related to a given company.  (Note: The code provided provides only the articles with summaries within 5 webpages (less than 10). it is done to save time in computing as it takes 10-15mins to run the code. if you need 10 article you can just remove the page variable in the code and proceed as is.)
- Performs **sentiment analysis** (Positive, Negative, Neutral).  
- Conducts **comparative sentiment analysis** to highlight differences in news coverage.  
- Extracts **key topics** from articles using zero-shot classification.  
- Converts the **summarized report into Hindi speech** using **Google Translate & gTTS**.  
- Provides a **user-friendly web interface** using **Streamlit**.  

---

## 2. Setup Instructions  

### Prerequisites  
Ensure you have **Python 3.8+** installed.  

### Step 1: Clone the Repository  
```bash
git clone https://github.com/your-repository/news-summarization-app.git
cd news-summarization-app
```

### Step 2: Install Dependencies  
```bash
pip install -r requirements.txt
```

---

## 3. Running the Application  

### Step 1: Start the FastAPI Backend  
Run the following command to start the backend server:  
```bash
uvicorn api:app --reload
```
This will start the **API server at `http://127.0.0.1:8000/`**.  

### Step 2: Start the Streamlit Frontend  
Open a new terminal and run:  
```bash
streamlit run app.py
```
This will launch the **web interface** where you can enter a company name and fetch results.

---

## 4. Testing the API (Optional)  
Before using the frontend, you can manually test the API by visiting:  
```txt
http://127.0.0.1:8000/news/?company=Tesla
```
This should return a **structured JSON response** with extracted news, sentiment scores, and topics.

To generate the **Hindi TTS audio**, visit:  
```txt
http://127.0.0.1:8000/tts/?company=Tesla
```

---


## 5. Technologies Used  
- **FastAPI**: For backend API development.  
- **Streamlit**: For frontend UI.  
- **BeautifulSoup4**: For web scraping.  
- **Sumy**: For text summarization.  
- **VADER Sentiment Analyzer**: For sentiment analysis.  
- **Transformers (Zero-shot Classification)**: For topic extraction.  
- **Google Translate & gTTS**: For Hindi speech synthesis.  

---
