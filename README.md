Project Summary
The AI Agent Dashboard is a web-based tool designed to process user-provided data (CSV files or Google Sheets), perform web searches, and extract insights using AI-powered natural language models. It enables efficient data exploration and analysis by integrating multiple APIs and streamlining complex workflows.
Key Features:-
File Upload: Upload CSV files and process their data.
Google Sheets Integration: Connect to and extract data from Google Sheets
AI-Powered Processing: Leverages OpenAI's GPT-3 to process entities and provide contextual insights.
Web Search Integration: Uses SerpAPI to retrieve web search results dynamically.
Results Download: Processed results can be downloaded as a CSV file
Responsive Design: User-friendly interface with animations for seamless interaction.

Setup Instructions
Clone the Repository
git clone https://github.com/Webdesigner4everyone002/AI-Agent-Dashboard

Install Dependencies
Create a virtual environment:
python3 -m venv venv
source venv/bin/activate  # For Linux/macOS
venv\Scripts\activate     # For Windows

Install required Python packages:
pip install -r requirements.txt

Configure API Keys
OpenAI API Key:
Obtain your API key from OpenAI.
Set it in the utils/llm_processing.py file:
openai.api_key = "YOUR_OPENAI_API_KEY"

SerpAPI Key:
Obtain your API key from SerpAPI.
Set it in the utils/web_search.py file:
api_key = "YOUR_SERPAPI_KEY"
Google Sheets API:
Generate a credentials.json file from the Google Cloud Console (enable the Sheets API and Drive API).
Place credentials.json in the project root directory.

4. Run the Application
python app.py
The app will be accessible at http://127.0.0.1:5000.

Usage Guide
Home Page
Access the main dashboard via the base URL.
Options:
Upload CSV: Select a file and click Upload CSV to process its data.
Upload Google Sheet: Enter the URL of your Google Sheet and click Upload Google Sheet.
Process Data
After uploading, choose a column from the displayed list.
Enter a query template (e.g., Summarize information about {entity}.).
Click Process Data to generate insights using the OpenAI GPT model and search results.
Download Results
Once the data is processed, click Download Results to save the output as a CSV file.

Third-Party APIs and Tools
OpenAI GPT-3:

Powers natural language understanding and generation.
Documentation.
SerpAPI:

Enables dynamic web searches.
Documentation.
Google Sheets API:

Allows integration with Google Sheets for data import.
Documentation.
Flask:

Backend framework to build the web app.
Documentation.

File structure:
ai-agent-dashboard/
│
├── app.py                   # Main Flask app
├── templates/
│   └── index.html           # Frontend HTML template
├── static/
│   ├── css/
│   │   └── style.css        # Styling for the dashboard
│   ├── js/
│   │   └── index.js         # Client-side JavaScript logic
├── utils/
│   ├── google_sheets.py     # Google Sheets integration
│   ├── web_search.py        # SerpAPI integration
│   ├── llm_processing.py    # OpenAI GPT-3 interaction
│   └── file_handling.py     # CSV file saving
├── requirements.txt         # Required Python packages
├── credentials.json         # Google Sheets API credentials
└── README.md                # Documentation

Future Improvements
Enhanced NLP Models: Integrate OpenAI GPT-4 for better insights.
Authentication: Add user authentication for secure API key management.
Asynchronous Processing: Use Celery to handle long-running tasks.
Extended Output Formats: Support additional formats like Excel or JSON.

Contributing
Feel free to fork the repository and submit pull requests. Contributions are welcome!
