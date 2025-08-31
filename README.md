# Market Intelligence AI Agent (n8n Workflows)

Automated **n8n workflows** that collect real-time market data, enrich it using LLMs, and deliver actionable insights to your workspace or Google Sheets.

---

## 🚀 Features
- **Agent Orchestration**: Main workflow coordinates all supporting flows.  
- **Web Data Collection**: Uses Bright Data and HTTP Request nodes to scrape competitor sites, news, and market updates.  
- **AI Enrichment**: LLM-powered summarization, classification, and scoring of raw data.  
- **Output Interface**: Pushes processed results into Google Sheets or chat UI.  

---

## 🧩 Workflows

| File                  | Purpose |
|-----------------------|---------|
| `workflows/main-agent.json`   | Orchestrates jobs, routes data to helper workflows, aggregates results. |
| `workflows/scraper.json`      | Scrapes websites, APIs, or Bright Data sources. |
| `workflows/enrichment.json`   | Uses LLM (OpenAI/Gemini) to parse, summarize, and enrich raw data. |
| `workflows/updater.json`      | Writes cleaned insights back to Google Sheets / sends chat updates. |

---

## 📁 Repo Structure

workflows/
├── main-agent.json
├── scraper.json
├── enrichment.json
└── updater.json

env/.env.example
docs/
└── architecture.png # Add your architecture diagram here
README.md
LICENSE
.gitignore


---

## 🛠️ Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/brightdata-n8n-agent.git
   cd brightdata-n8n-agent

2. Set environment variables
Copy env/.env.example → env/.env and fill in your keys:

BRIGHT_DATA_API_KEY=your_key
OPENAI_API_KEY=your_key
GEMINI_API_KEY=your_key


3. Import into n8n

In n8n → Workflows → Import from File → select JSONs from /workflows/.

Update credentials in n8n Credentials UI (Bright Data, Google Sheets, LLM, etc.).

4. Run the agent

Execute main-agent.json → it will trigger the scraper, enrichment, and updater flows.

---


## 🎬 Demo / Live Access

Demo Video: [Add Loom/YouTube link here]

---

## 📷 Architecture Diagram

<img width="808" height="338" alt="image" src="https://github.com/user-attachments/assets/8cf60994-0330-4a09-bbd4-0507e928ed43" />


# 🧾 License

This project is licensed under the MIT License – see [LICENSE](LICENSE).
