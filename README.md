# Data Analyst Agent - AI-Powered Data Companion  
> Smarter, faster, and more intuitive analysis of your datasets using **Generative AI + Python.**  

---

## What Is This?  
Meet the **Data Analyst Agent** - an AI-driven assistant that eliminates tedious data crunching.  
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
**Write Your Questions**
Example:
What’s the revenue growth month-over-month?
Find correlation between Age and Income
Show most profitable products
**Upload Dataset + Questions File**
Dataset (optional): CSV, Excel, JSON, Parquet, or TXT
Questions file (required): Plain text
**Get Results**
AI processes the queries
Generates insights and summaries
Builds visualizations automatically

# About the Project
Project: AI Data Analyst Agent — an autonomous data analysis platform that accepts datasets (CSV, Excel, JSON, Parquet, images) and natural language questions, then generates insights, visualizations, and structured answers without requiring users to write code.

Problem: Non-technical users struggle to extract insights from raw data. This agent bridges the gap by converting natural language queries into executable Python analysis code over uploaded datasets.

LLMs Used: Google Gemini family (gemini-2.5-pro, 2.5-flash, 2.5-flash-lite, 2.0-flash, 2.0-flash-lite) with a custom fallback hierarchy across 10 API keys for load balancing and fault tolerance.

Tools/Frameworks: FastAPI, LangChain (agent orchestration), DuckDB (in-memory SQL), Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Pillow. Deployed via Docker/Heroku.

Architecture: Agent-based code generation pattern — the LLM receives a dataset preview (columns + sample rows) as context augmentation, generates executable Python code, which is then sandboxed and executed. A scrape_url_to_dataframe tool enables dynamic web data retrieval when no dataset is uploaded.

Hallucination Control: Temperature set to 0 for deterministic outputs, strict structured JSON output enforcement, robust JSON parsing with fallback scanning, code execution as an implicit correctness filter (generated code must run without errors), explicit system prompt constraints, and type-casting validation on results.

Evaluation: System diagnostics endpoint validates LLM connectivity, key health, pandas pipeline integrity, DuckDB functionality, and network reachability. Code execution success/failure serves as runtime validation.

Note: This is not a traditional vector-search RAG pipeline — it uses a direct context-augmentation approach where the full dataset preview is injected into the LLM prompt, and the LLM generates analysis code rather than retrieving from a document store. This is more suitable for structured data analysis where the dataset fits in memory.
