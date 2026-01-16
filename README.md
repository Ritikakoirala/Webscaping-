TutorialsFreak Web Scraper
A Python-based web scraping utility that extracts structured data from the TutorialsFreak homepage.
This project demonstrates how to fetch web content, parse HTML, navigate the DOM, and extract useful data such as links, images, and course information.

📌 Project Overview

This web scraper uses:

Requests → to fetch web content

BeautifulSoup4 → to parse and navigate HTML

🎯 Data Extracted
🔹 Metadata

Page Title

Website URL

HTTP Status Code (e.g., 200 OK)

🔹 Content Elements

All paragraph tags (<p>)

All anchor tags (<a>)

Main heading (<h1>)

🔹 Structured Course Data

Course titles

List items inside specific card elements

🔹 Media

All image source (src) URLs
💻 Code Breakdown

The scraper follows a standard web scraping workflow:

1️⃣ Request

Fetches HTML content from the TutorialsFreak website using requests.get().

2️⃣ Parse

Converts raw HTML into a searchable BeautifulSoup object.

3️⃣ Navigate

Accesses specific sections like:

<head>

<body>

4️⃣ Filter

Uses find() and find_all() to locate:

Tags (p, a, h1, img)

Specific classes (e.g., .card-haed)

5️⃣ Clean & Extract

.text → human-readable content

.get("href"), .get("src") → attribute values
