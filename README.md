# 📚 EduTrack LangGraph

**EduTrack LangGraph** is an AI-powered assistant built with **LangGraph**, **LangChain**, and **Streamlit**. It dynamically processes student queries, routes them to intelligent agents (Academic, Career, Wellness, and Performance), and delivers personalized recommendations by grounding responses in structured CSV datasets.

---

## 🚀 Features

- 🔍 **Automatic Agent Routing** – Detects query intent using LLMs and activates only relevant agents.
- 🗂️ **Multi-Source Data Extraction** – Integrates information from multiple `*_refined.csv` files.
- 🧠 **Contextualized LLM Prompts** – Agent replies are grounded in the student's profile.
- 🌐 **Interactive Frontend** – Powered by Streamlit for live query interaction and detailed agent responses.

---

## 📁 Required Datasets

Place the following CSV files in the project root:

- `academic_refined.csv`
- `performance_refined.csv`
- `welfare_refined.csv`
- `career_refined.csv`

Each should include a `student_id` or `name` column for identification.

---

## ⚙️ Installation

```bash
# Clone the repository
git clone https://github.com/your-repo/edutrack-langgraph
cd edutrack-langgraph

# Install dependencies
pip install streamlit pandas langchain langgraph langchain_groq
