# Blogger AI 🚀🤖

A simple Flask-based multi-agent system using [CrewAI](https://github.com/joaomdmoura/crewai), [LangChain](https://www.langchain.com/), and OpenAI. This project demonstrates how multiple LLM agents can collaborate to generate insightful content such as blogs from a given task.

---

## 🔧 Features

- 🔁 Multi-agent collaboration using CrewAI.
- 🧠 Agents built on top of LangChain and GPT-4.
- 🌐 Flask server with a `/run` endpoint to trigger blog generation.

---

## 📁 Folder Structure

<pre> ``` crew-ai-flask-starter/ ├── app.py # Flask server with /run endpoint ├── agents.py # Agent definitions and Crew setup ├── requirements.txt # Python dependencies └── .env # OpenAI API key ``` </pre>




---

## 🧪 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/crew-ai-flask-starter.git
cd crew-ai-flask-starter
````

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory with your OpenAI key:

```env
OPENAI_API_KEY=your-openai-api-key-here
```

---

## ▶️ Running the App

Start the Flask server:

```bash
python app.py
```

Visit your browser at: [http://localhost:5000](http://localhost:5000)

---

## 📡 API Endpoint

### POST `/run`

Trigger a blog post generation via a JSON request.

#### Request Format

```json
{
  "task": "Write a blog post about Artificial Intelligence"
}
```

#### Example `curl` Command

```bash
curl -X POST http://localhost:5000/run \
-H "Content-Type: application/json" \
-d '{"task": "Write a blog post about Artificial Intelligence"}'
```

#### Response

Returns the blog post as HTML rendered in the browser.

---

## 🤖 Agents

* **Planner** – Expert in gathering detailed information about a topic.
* **Writer** – Specializes in converting complex content into digestible summaries.

---

## 🧩 Technologies Used

* [CrewAI](https://github.com/joaomdmoura/crewai)
* [LangChain](https://www.langchain.com/)
* [OpenAI GPT-4](https://platform.openai.com/)
* [Flask](https://flask.palletsprojects.com/)

---

## 💡 Inspiration

Inspired by the need to automate content generation using autonomous AI agents that can collaborate with minimal human input.

---

## 📜 License

MIT License

---

> Built with ❤️ for experimenting with AI agent collaboration and content generation.

```
