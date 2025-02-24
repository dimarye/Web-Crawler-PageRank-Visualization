Web Crawler & PageRank Visualization

Overview

This project is a simple web crawler that collects links from a given website, stores them in a database, and calculates their importance using the PageRank algorithm. The results are visualized in an interactive force-directed graph using D3.js.

Features

🕷 Web Crawler – Scrapes links from a website and stores them in an SQLite database.

🔢 PageRank Calculation – Iteratively computes PageRank scores for collected URLs.

📊 Data Export – Generates a JSON file with network data for visualization.

🌍 Interactive Graph – Displays link relationships using a D3.js force-directed graph.

Installation

Clone the repository:

git clone https://github.com/yourusername/web-crawler-pagerank.git
cd web-crawler-pagerank

Install dependencies:

pip install -r requirements.txt

Usage

1️⃣ Run the Web Crawler

python spider.py

Enter a starting URL

Specify the number of pages to crawl

2️⃣ Compute PageRank

python spreset.py  # Reset PageRank values
python sprank.py   # Compute new PageRank scores

3️⃣ Export Data for Visualization

python spjson.py

4️⃣ View the Graph

Open force.html in a browser to explore the link structure visually.

Future Improvements

🔹 Async crawling with aiohttp for faster performance
🔹 Web-based UI for controlling the crawler and viewing results
🔹 Export data to Neo4j for advanced network analysis

License

📜 MIT License – Free to use and modify.
