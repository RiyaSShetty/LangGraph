EduTrack LangGraph

EduTrack LangGraph is an intelligent, agent-powered assistant for analyzing and advising student progress using modular agents with LangGraph and Streamlit. It processes student queries in real-time and activates relevant agents to provide grounded feedback from structured CSV datasets.

🧠 Core Capabilities

Automatic Agent Routing: Detects query intent and activates suitable agents

Multi-Source Data Extraction: Pulls relevant student data from multiple *_refined.csv datasets

Contextualized LLM Prompts: Each agent responds with domain-specific recommendations

Streamlit Frontend: User-friendly interface for asking queries and viewing agent responses

📂 Required CSV Files

Ensure the following refined CSVs are present in the same directory:

academic_refined.csv

performance_refined.csv

welfare_refined.csv

career_refined.csv

🔧 Installation & Setup

Clone the repo or copy the script edutrack_app.py

Install the required dependencies:

pip install streamlit pandas langchain langgraph langchain_groq

Make sure you have a valid Groq API Key and replace it in edutrack_app.py

Run the Streamlit app:

streamlit run edutrack_app.py

🤖 Agent Roles

Agent Name

Purpose

academic_agent

GPA, study strategy, time management, course feedback

performance_agent

Weak/strong subjects, test progress, personalized improvement plans

career_agent

Career advice, internships, resume tips, skill-building suggestions

wellness_agent

Stress, mental health, self-care, well-being suggestions

💬 Example Query

"How can Ankit R with ID 1001 improve his GPA and prepare for a Cloud Engineer role?"

Expected Behavior:

Extracts Ankit's data from all datasets

Detects and activates academic_agent, performance_agent, and career_agent

Displays combined recommendations from each

🎨 Customization

To Customize Agent Output Style:

Edit the summary = f"..." blocks inside each agent function to modify what data gets shown.

To Increase Font Size of Agent Names:

In Streamlit UI loop:

st.markdown(f"""<h4 style='font-size:24px;'>{msg['sender']}</h4><p>{msg['content']}</p>""", unsafe_allow_html=True)

Replace this line:

st.markdown(f"**{msg['sender']}**\n\n{msg['content']}")

📊 Metrics Displayed

Execution time

Number of agents invoked

Number of inter-agent communications

Detailed agent log trace

📌 Notes

Agent responses are grounded using combined user data

If no match found, fallback logic still runs AcademicAgent

You can easily plug in additional agents or models

🔮 Future Enhancements

User authentication for student history

Graphical performance dashboard

PDF export of agent recommendations

Integrated scheduling or follow-ups

🧠 Built With

LangGraph

Streamlit

Groq + Llama3