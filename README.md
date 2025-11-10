# 🧠 AI Research Assistant

An **AI-powered research assistant** that automatically gathers, summarizes, and structures research information using the **LangChain framework** and **Anthropic’s Claude model**.  
It uses **Wikipedia** and **DuckDuckGo Search** as knowledge tools and can **save results automatically** in a structured format.

---

## 🚀 Features

- 🤖 **LLM-powered research** using Anthropic Claude 3.5 Sonnet  
- 🔍 **Web and Wikipedia integration** for comprehensive research  
- 🧩 **Tool-based modular design** via LangChain agents  
- 🗂️ **Structured output** (topic, summary, sources, tools used) with Pydantic  
- 💾 **Automatic saving** of research results to text files  

---

## 🧰 Tech Stack

| Component | Description |
|------------|-------------|
| **Python** | Core programming language |
| **LangChain** | Framework for LLM-based agents and tools |
| **Anthropic Claude 3.5 Sonnet** | Large Language Model for research reasoning |
| **DuckDuckGo Search API** | For live web results |
| **Wikipedia API** | For structured encyclopedia summaries |
| **Pydantic** | To define structured output models |
| **dotenv** | For managing API keys and environment variables |

---

## 📁 Project Structure

```
├── main.py               # Main script to run the research assistant
├── tools.py              # Custom tools (search, wiki, save)
├── requirements.txt      # Python dependencies
└── research_output.txt   # Output file (generated after running)
```

---

## ⚙️ Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/<your-username>/ai-research-assistant.git
   cd ai-research-assistant
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate    # macOS/Linux
   venv\Scripts\activate       # Windows
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables:**
   Create a `.env` file in the project root and add your Anthropic API key:
   ```
   ANTHROPIC_API_KEY=your_api_key_here
   ```

---

## ▶️ Usage

Run the main script:
```bash
python main.py
```

Then, when prompted:
```
What can I help you research?
```

Type your research topic (e.g., *Quantum computing in AI*).  
The program will:
1. Query DuckDuckGo and Wikipedia.
2. Generate a structured research summary.
3. Print and save the results automatically in `research_output.txt`.

---

## 📦 Example Output

```text
--- Research Output ---
Timestamp: 2025-11-10 18:42:21

Topic: Quantum Computing in Artificial Intelligence
Summary: Quantum computing introduces parallel computation advantages...
Sources: ["Wikipedia", "DuckDuckGo Search"]
Tools Used: ["wiki_tool", "search_tool", "save_tool"]
```

---

## 🧩 How It Works

| Step | Description |
|------|-------------|
| 1️⃣ Load environment and dependencies | `.env`, Anthropic API, LangChain tools |
| 2️⃣ Define a Pydantic model | Ensures structured research output |
| 3️⃣ Initialize LLM and tools | Claude 3.5 Sonnet + Wikipedia + DuckDuckGo |
| 4️⃣ Create an agent executor | Handles reasoning and tool calling |
| 5️⃣ Process query | AI uses tools to gather and summarize data |
| 6️⃣ Save results | Output is written to a timestamped text file |

---

## 🧠 Future Improvements

- Add more specialized knowledge tools (e.g., Arxiv, Semantic Scholar)
- Enable PDF export for research reports
- Integrate a Streamlit or Gradio UI
- Add citation formatting (APA/IEEE style)

---

## 📜 License

This project is open-source and available under the **MIT License**.
