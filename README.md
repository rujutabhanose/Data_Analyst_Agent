# Data Analyst Agent — Your AI-Powered Data Companion  
> Smarter, faster, and more intuitive analysis of your datasets using **Generative AI + Python.**

---

## What Is This?  
Meet **Data Analyst Agent 2.0** — an AI-driven assistant that eliminates tedious data crunching.  
Upload your dataset and queries to instantly get:  
- Visual reports  
- AI-generated insights  
- Automated workflows  

Perfect for:  
- Analysts  
- Researchers  
- Startups & Businesses  
- Anyone who loves turning raw data into knowledge  

---

## Key Highlights  

| Feature              | Why It’s Awesome |
|-----------------------|------------------|
| AI-Powered Insights   | Uses Google’s Generative AI to “understand” your data |
| Rich Visualizations   | Generates plots with **Seaborn & Matplotlib** |
| Web Scraper Mode      | Fetch live data directly from URLs |
| Multi-Format Friendly | Accepts CSV, Excel, JSON, Parquet, or TXT |
| Batch Processing      | Ask multiple questions at once |
| Simple Interface      | Beginner-friendly, no steep learning curve |
| Fast Execution        | Optimized for speed and real-time feedback |

---

## Getting Started  

### 1. Clone the Repo  
```bash
git clone https://github.com/rujutabhanose/Data_Analyst_Agent.git
cd Data_Analyst_Agent
```

### 2. Install Requirements
pip install -r requirements.txt

### 3. Configure API Keys
Create a .env file inside the root folder:
GEMINI_API_KEY=your_google_api_key
LLM_TIMEOUT_SECONDS=240

### 4. Start the Application
python3 -m uvicorn app:app --reload
Then open http://localhost:8000/ in your browser.

# How It Works
Write Your Questions
Example:
What’s the revenue growth month-over-month?
Find correlation between Age and Income
Show most profitable products
Upload Dataset + Questions File
Dataset (optional): CSV, Excel, JSON, Parquet, or TXT
Questions file (required): Plain text
Get Results
AI processes the queries
Generates insights and summaries
Builds visualizations automatically
