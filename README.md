# 🎬 Movie Recommendation Chatbot

An AI-powered chatbot that recommends movies based on user queries using **Neo4j, Python, SpaCy, and Gradio**.

---

## 🚀 Features

✅ **Natural Language Processing (NLP)**: Uses **SpaCy** to extract movie names from user queries.  
✅ **Graph Database Integration**: Utilizes **Neo4j** to find and recommend movies based on shared actors.  
✅ **Cypher Query Execution**: Dynamically constructs and executes queries to fetch relevant movie recommendations.  
✅ **Interactive Chatbot**: Built with **Gradio** for an easy-to-use conversational interface.  
✅ **Fast & Scalable**: Leverages graph databases for quick movie recommendations.

---

## 🛠️ Tech Stack

- **Python** 🐍
- **Neo4j** (Graph Database) 🗃️
- **SpaCy** (NLP Processing) 🧠
- **Gradio** (Chatbot UI) 💬
- **Cypher** (Query Language) 🔍

---

## 📌 Installation & Setup

### 1️⃣ Clone the Repository
```bash
$ git clone https://github.com/your-username/movie-chatbot.git
$ cd movie-chatbot
```

### 2️⃣ Install Dependencies
```bash
$ pip install -r requirements.txt
```

### 3️⃣ Run Neo4j Database
Ensure that you have Neo4j installed and running. You can also use a Neo4j sandbox:
```bash
$ neo4j start
```

Update the `BOLT_URL`, `USERNAME`, and `PASSWORD` in the Python script accordingly.

### 4️⃣ Run the Chatbot
```bash
$ python chatbot.py
```
This will launch a Gradio UI where you can interact with the chatbot.

---

## 🔗 Cypher Query Used
```cypher
MATCH (movie:Movie {title:$favorite})<-[:ACTED_IN]-(actor)-[:ACTED_IN]->(rec:Movie)
RETURN distinct rec.title as title LIMIT 20
```
This query finds movies related to the user's favorite movie by identifying actors who have acted in both.

---

## 📸 Demo
![Chatbot Screenshot](screenshot.png) *(Replace with an actual screenshot of the chatbot UI)*

---

## 🤖 How It Works
1. The user enters a movie title.
2. **SpaCy** extracts the movie name from the text.
3. **Neo4j** runs a Cypher query to fetch recommended movies.
4. The chatbot returns the recommended movie list.

---

## 🤝 Contributing
Want to improve this chatbot? Feel free to open an issue or submit a pull request!

---

## 📜 License
This project is licensed under the MIT License.

---

## 🌟 Show Some Love
If you like this project, give it a ⭐ on [GitHub](https://github.com/your-username/movie-chatbot)! 😊

