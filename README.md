Web Crawler and Search Engine

#Project Overview
This project is a Python-based **Web Crawler and Mini Search Engine**.  
It crawls web pages using multiple workers, processes the collected pages, builds an **inverted index with TF-IDF**, and provides a **Flask-based web interface** to search and rank documents.

---

#Features
- Multi-worker web crawling
- URL queue handling using RabbitMQ
- HTML parsing and text extraction
- Inverted index creation
- TF-IDF based ranking
- Simple search UI using Flask

---

#Technologies Used
- Python
- BeautifulSoup
- Requests
- RabbitMQ
- Flask
- HTML & CSS
- TF-IDF Algorithm
---
  Project Structure
└── crawler/
├── crawler.py
├── producer.py
├── worker.py
├── indexer.py
├── inverted_index.json
├── idf.json
├── pages/
└── search_app/
├── app.py
├── templates/
│ └── index.html
└── static/
└── style.css
---
How to Run the Project
Install Required Libraries
*pip install requests beautifulsoup4 flask pika
Start RabbitMQ Server
Ensure RabbitMQ is running on:localhost:5672
Run the Web Crawler: 
python producer.py
python worker.py(HTML pages will be saved inside the pages/ folder)
python indexer.py








## 📂 Project Structure
