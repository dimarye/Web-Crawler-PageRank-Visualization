Web Crawler & PageRank Visualization

Overview

This project is a simple web crawler that collects links from a given website, stores them in a database, and calculates their importance using the PageRank algorithm. The results are visualized in an interactive force-directed graph using D3.js.

Features

🕷 Web Crawler – Scrapes links from a website and stores them in an SQLite database.

🔢 PageRank Calculation – Iteratively computes PageRank scores for collected URLs.

📊 Data Export – Generates a JSON file with network data for visualization.

🌍 Interactive Graph – Displays link relationships using a D3.js force-directed graph.


This code crawls web pages, saves them in a database, builds a link graph, and then computes PageRank (Google's algorithm for ranking pages).

## Main Workflow
### 1️⃣ Collecting Links (`spider.py`)
- Loads a web page
- Extracts links
- Saves them into `spider.sqlite` database

### 2️⃣ Preparing Data (`spreset.py`)
- Resets all PageRank values to 1.0

### 3️⃣ Computing PageRank (`sprank.py`)
- Iteratively updates page rankings
- The more incoming links a page has, the higher its rank

### 4️⃣ Generating JSON for Visualization (`spjson.py`)
- Creates `spider.js`, containing nodes and link relationships

### 5️⃣ Displaying Results (`spdump.py`)
- Shows pages with the highest number of incoming links

### 6️⃣ Visualization (`force.html + force.js + force.css`)
- `force.html` loads `spider.js` and visualizes the link graph using **D3.js**

## How to Run the Project
### **Step 1: Start the Crawler**
```bash
python spider.py
```
- Enter a **URL** (e.g., `https://example.com`)
- Specify how many pages to crawl

### **Step 2: Update PageRank**
```bash
python spreset.py
python sprank.py
```
- (Specify the number of iterations when running `sprank.py`.)

### **Step 3: Generate JSON for Visualization**
```bash
python spjson.py
```
- (Enter the number of nodes to include in the graph.)

### **Step 4: Open `force.html` in a Browser**
- Open the `force.html` file
- An interactive link graph should appear

