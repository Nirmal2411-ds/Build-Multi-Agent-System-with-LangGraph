# Build-Multi-Agent-System-with-LangGraph

🧠 Multi-Agent AI Research & Writing System using LangGraph

A production-style Agentic AI workflow where specialized agents collaborate like a newsroom — one researches, one writes.

Traditional LLM applications rely on a single prompt to perform complex tasks. This often leads to hallucinations, poor reasoning traceability, and limited scalability. Real-world AI systems require modular workflows, tool usage, and controlled information passing between multiple decision points.


Design and implement a multi-agent architecture where:
One agent gathers grounded, real-time information from the web.
Another agent synthesizes the information into a structured output.
The system enforces deterministic flow, shared memory, and reliable execution.
The goal was to simulate how cross-functional teams collaborate while minimizing hallucination and maximizing explainability.

🏗 Architecture  
The workflow follows a relay model:  
User Topic  
   ↓  
[Researcher Agent]  → fetches facts  
   ↓  
[Writer Agent]      → synthesizes content  
   ↓  
Final Blog Post  

🧶Components  
- Nodes → agents / functions  
- Edges → execution order  
- State → shared memory  


⚙️ Tech Stack  
- Python  
- LangGraph  
- LangChain  
- Ollama  
- Llama 3  
- DuckDuckGo Search  
- TypedDict state management  

📁 Project Structure  
multi-agent-langgraph/  
│
├── requirements.txt 
├── multi_agent.py
└── README.md  

✅ Prerequisites

You need:  
- Python 3.9+  
- Ollama installed  
- Internet for search tool  

Install Ollama  
Download from:  
👉 https://ollama.com  

Pull the model  
ollama pull llama3  

📦 Installation  
1️⃣ Clone repo  
git clone https://github.com/yourusername/multi-agent-langgraph.git  
cd multi-agent-langgraph  

2️⃣ Create a virtual environment (recommended)  
- python -m venv venv  
- source venv/bin/activate     # mac/linux  
- venv\Scripts\activate        # windows  

3️⃣ Install dependencies  
pip install -r requirements.txt  


If needed:  
pip install langgraph langchain langchain-community langchain-ollama duckduckgo-search  

Task:  
- Design and implement a multi-agent architecture where:
- One agent gathers grounded, real-time information from the web.
- Another agent synthesizes the information into a structured output.
- The system enforces deterministic flow, shared memory, and reliable execution.
- The goal was to simulate how cross-functional teams collaborate while minimizing hallucination and maximizing explainability.

Action:  
- I built a LangGraph-powered orchestration pipeline with:
- Typed shared state for safe inter-agent communication
- A Research Agent using live search (DuckDuckGo)
- A Writer Agent powered by a local LLM (Llama 3 via Ollama)
- Sequential routing of tasks via graph edges
- Structured prompts enforcing grounded generation
- Modular nodes that can be extended into reviewer/critic agents
- The system separates data acquisition from reasoning, improving factual accuracy and reducing cost.  

📜 License  
MIT  

▶️ How to Run  
python main.py  

Example Console Output:   
Starting the Multi-Agent System...  
Researcher is looking up: The future of AI Agents...  
Research complete.  
Writer is drafting the post...  
Writing complete.  
---------------- FINAL OUTPUT ----------------  
<Generated blog appears>  
