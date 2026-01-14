TutorialsFreak Web ScraperA Python-based web utility that extracts structured data from the TutorialsFreak homepage.
This script demonstrates how to parse HTML, navigate tags, and extract specific attributes like links and image sources.
📌 Project OverviewThis project uses Requests to fetch web content and BeautifulSoup4 to parse the DOM. 
It specifically targets:Metadata: Title, URL, and Status Codes.Content: All paragraph (<p>), anchor (<a>), and header (<h1>) tags.Structured Data: 
Course titles and list items inside specific card elements.Media: All image source (src) URLs.
🛠️ RequirementsEnsure you have the following Python libraries installed:Bashpip install requests beautifulsoup4
💻 Code BreakdownThe scraper follows a standard extraction workflow:Request: Fetches the HTML content from the server.
Parse: Converts the raw HTML into a searchable "Soup" object.Navigate: Accesses specific tags (like .body or .head
).Filter: Uses find_all() to isolate specific classes or elements.Clean: Uses .text and .get() to retrieve human-readable data.
Key SnippetsTo find specific course headers and lists within cards:Pythonall_divs = body.find_all("div", class_="card-haed")
for div in all_divs:
    print(div.find("h3").text)
    print(div.find("ul").text)
🚀 How to RunClone this repository.Open your terminal or IDE.Run the script:Bashpython scraper.py
📊 Extracted Data PointsElementExtraction MethodPurposeStatus Codeweb.status_codeConfirms if the site is reachable (e.g., 200).
Linkssoup.find_all("a")Extracts all hyperlinks from the page.Imagesimg.get("src")Collects paths to all visual assets.Cards.card-haedTargets specific content blocks for titles/lists.
