<h1 align="center"> 🤖📚 ArxivAgent: Multi-Agent ArXiv Paper Finder </h1>

## 📝 Project Overview

ArxivAgent is a multi-agent AI tool built with Microsoft's AutoGen framework that automates the process of finding and summarizing research papers from ArXiv. Designed for researchers, students, and developers, the project leverages GPT-4o-powered agents to search for relevant papers and produce structured summaries in a literature review format.

## 🎯 Key Features

* 🔍 **Automated ArXiv Search**: Finds relevant papers using keywords intelligently extracted from user queries.
* 📄 **Summarization**: Produces clean, structured summaries with titles, key contributions, and direct ArXiv links.
* 🧠 **Multi-Agent Architecture**: Utilizes AutoGen's RoundRobinGroupChat to coordinate between a Researcher Agent and a Summarizer Agent.
* 🧰 **Backend-Only Functionality**: Fully working via local scripts, designed for future integration with a Streamlit frontend.

## 🧠 Agents

* **Researcher Agent**: Extracts keywords and queries ArXiv using a custom API tool.
* **Summarizer Agent**: Takes paper metadata and formats a clear summary in literature review style.

## ⚙️ Technologies Used

* Microsoft AutoGen (Multi-Agent Framework)
* GPT-4o (via OpenAI)
* Python 3.12
* ArXiv API

## 🗂️ Project Structure

```
ARXIV-PAPER-FINDER/
├── autogen-arxiv-researcher/        # Python virtual environment
├── agent_backend.py                 # Backend for summarization
├── .env                             # API keys (ignored)
├── requirements.txt                 # Project dependencies
├── LICENSE.txt                      # License file (MIT)
└── README.md                        # You're here
```

## 🚀 Getting Started

1. Clone the repo:

```bash
git clone https://github.com/kunalmishravitb/ArxivAgent.git
cd ArxivAgent
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Add your OpenAI API key in a `.env` file:

```
OPENAI_API_KEY=your_key_here
```

4. Run the app:

```bash
python agent_backend.py
```

## 🔍 Example Query

```
Topic: "Agentic AI"
Response:
- Title: Architectures for Agentic Collaboration
- Key Contributions: Proposes a novel loop-based coordination method for LLM agents...
- ArXiv: https://arxiv.org/abs/xxxx.xxxxx
```

## 🛠 Configuration

Edit the following lines in `agent_backend.py` to change the behavior:

```
topic = "Autogen"  # change this to your topic of interest
task = f"Conduct a literature review on the topic - {topic} and return exactly 1 Papers."
```

You can also adjust the number of papers requested.

## 🔧 Future Improvements

* ✅ Streamlit Frontend (WIP)
* 📚 Filter by paper date, category
* 🧪 Evaluate summary quality against ground truth

## 🤝 Acknowledgements

* Microsoft AutoGen Team for enabling multi-agent capabilities
* OpenAI GPT-4o for accurate summarization

---

Built by [Kunal Mishra](https://github.com/kunalmishravitb) to make research faster and smarter.
