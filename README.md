# Subscription-Tracker
This n8n workflow automatically tracks subscription/recurring expenses. When the user sends a natural language message (e.g., “I subscribed to Spotify for $9.99 a month”), the workflow extracts details and appends them into a Google Sheet.

* Features

- Extracts subscription details (Expense, Charge Date, Cadence, Cost, Status)

- Default values applied (e.g., today’s date if no charge date given)

- Appends to Google Sheets (or Excel/CSV alternative if Ollama is used)

- Runs locally with Ollama (free) or with OpenAI/Claude/Gemini APIs

* Requirements

- n8n installed (self-hosted or n8n.cloud)

- Ollama (local model) or OpenAI/Claude API key (if tool support required)

- Google Sheets API credentials (if using Google Sheets node)

* Setup Instructions

- Clone this repo.

- Open n8n editor.

- Import the workflow JSON (Import from file).

* Configure credentials:

- Google Sheets OAuth (if using Sheets).

- Ollama (ensure model like llama3 is downloaded).

- Run workflow.

* Usage

Send a message like:

"I just subscribed to Netflix for $15 per month"

* Customization

- You can switch storage from Google Sheets → Excel/CSV using the Spreadsheet node.

- Cadence defaults to Monthly but can be changed.

- Status defaults to Active unless cancelled/paused is mentioned.
