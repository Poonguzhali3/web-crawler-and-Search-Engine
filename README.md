Web Crawler and Search Engine

#Project Overview
This project is a Python-based Web Crawler and Mini Search Engine.  
It crawls web pages using multiple workers, processes the collected pages, builds an inverted index with TF-IDF, and provides a Flask-based web interface to search and rank documents.

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

How to Run the Project
Install Required Libraries
*pip install requests beautifulsoup4 flask pika
Start RabbitMQ Server
Ensure RabbitMQ is running on:localhost:5672
Run the Web Crawler: 
python producer.py
python worker.py(HTML pages will be saved inside the pages/ folder)
python indexer.py(This generates:inverted_index.json,idf.json)
python app.py
Go to:http://127.0.0.1:5000

---
How Search Works:
User query is tokenized
TF (Term Frequency) is taken from the inverted index
IDF (Inverse Document Frequency) is applied
Documents are ranked using TF × IDF

---
Conclusion:
This project implements a web crawler and search engine using Python. It collects web pages, builds an inverted index with TF-IDF, and provides a Flask-based search interface. The project demonstrates core concepts of web crawling, indexing, and information retrieval.





