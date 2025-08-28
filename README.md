AI Job Mailer ✉️

AI Job Mailer is an LLM-powered cold email generator that scrapes job postings, extracts key details, cross-references them with a stored portfolio, and automatically generates tailored cold emails for business development outreach. Built with LangChain, Fireworks LLM, ChromaDB, and Streamlit, this tool streamlines lead generation for consulting and software service firms.

🚀 Features

 Job Scraping – Extract job postings directly from career pages.

 Job Role Extraction – Use LLMs to identify role, skills, experience, and description.

 Portfolio Matching – Query a pre-stored project portfolio in ChromaDB to find the most relevant past work.

 AI-Powered Email Generation – Generate professional, context-aware cold emails using Fireworks LLM.

 Streamlit App – Simple web interface to enter job URLs and generate emails instantly.

🛠️ Tech Stack

Python

Streamlit – Web UI

LangChain – Orchestration

Fireworks LLM (Llama 3.1 8B Instruct) – Language model

ChromaDB – Portfolio storage & retrieval

Pandas – Portfolio dataset handling

Regex (utils.py) – Text cleaning

📂 Project Structure
AI-Job-Mailer/
│── appC.py            # Streamlit app entry point
│── chains.py          # LLM chains for job extraction & email generation
│── portfolio.py       # Portfolio class using ChromaDB
│── utils.py           # Text cleaning utilities
│── my_portfolio.csv   # Portfolio dataset (tech stack + links)
│── llamaproj.ipynb    # Notebook for testing and exploration
│── tech.txt           # Project notes
│── README.md          # Documentation

⚙️ Setup & Installation

Clone the repository:

git clone https://github.com/ArunSanyal/AI-job-mailer.git
cd AI-job-mailer


Create a virtual environment & install dependencies:

pip install -r requirements.txt


Add your Fireworks API key to a .env file:

FIREWORKS_API_KEY=your_api_key_here

▶️ Usage

Run the Streamlit app:

streamlit run appC.py


Enter a job posting URL in the input field.

The system will:

Scrape and clean job text

Extract job details (role, skills, description)

Query portfolio links from my_portfolio.csv via ChromaDB

Generate a tailored cold email

📊 Example Output

Input URL: A job posting for Lead GenAI Product Manager at Nike.

Generated Email:

Dear Hiring Manager,  

I came across your posting for a Lead GenAI Product Manager role, and I wanted to share how Konsultera can assist...  
[Relevant portfolio project links inserted here]  

Best regards,  
XYZ  
Business Development Executive, Konsultera  

🔮 Future Improvements

Add support for multi-page job scraping.

Improve portfolio ranking with semantic similarity scoring.

Extend output to multi-email sequences for outreach campaigns.

Deploy as a hosted web app.
