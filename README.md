🔍 Free Fire Like Bot


A Discord bot and Flask server that allows you to automatically like Free Fire profiles via their user ID.
Includes advanced features like channel restrictions, cooldowns, JSON config, and support for both RapidAPI and a self-hosted API.

📌 Table of Contents
🚀 Features

🧰 Requirements

⚙️ Installation

💬 Usage

🤖 Create a Discord Bot

🌐 Custom or Public API

📤 Example Output

🛠 Technologies Used

📄 License

👨‍💻 Author

🚀 Features
✅ /like <uid>: Send likes to Free Fire users.

🔐 /setlikechannel <channel>: Restrict usage to selected channels.

🔁 Per-user cooldown (30 seconds).

🧠 Channel config saved in like_channels.json.

📡 Flask web server at http://localhost:10000 for status.

🔑 Secure token/key storage via .env.

🌐 Choose between RapidAPI or your own hosted API.

📊 Embedded responses with like count before/after.

🧰 Requirements
Python 3.8+

A Discord bot token

A RapidAPI key or a self-hosted API server

A .env file containing:

ini
Copy
Edit
TOKEN=your_discord_bot_token
RAPIDAPI_KEY=your_rapidapi_key_or_custom_api_key
⚙️ Installation
Clone this repository:

sh
Copy
Edit
git clone https://github.com/mynibir/free-fire-like-bot
cd free-fire-like-bot
Create and activate a virtual environment:

sh
Copy
Edit
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
Install dependencies:

sh
Copy
Edit
pip install -r requirements.txt
Create a .env file in the root directory and add your credentials:

ini
Copy
Edit
TOKEN=your_discord_bot_token
RAPIDAPI_KEY=your_rapidapi_key_or_empty_if_custom
Run the bot:

sh
Copy
Edit
python app.py
💬 Usage
Use /like <user_id> in a Discord server where the bot is present.

Use /setlikechannel <channel> to toggle allowed channels for the like command.

🤖 Create a Discord Bot
Go to the Discord Developer Portal.

Click "New Application", and give your bot a name.

In the left sidebar, go to the "Bot" section and click "Add Bot", then confirm with "Yes, do it!".

Under the Token section, click "Reset Token" or "Copy" to get your TOKEN.

Go to "General Information" and copy the APPLICATION_ID.

Paste both values into your .env file:

ini
Copy
Edit
TOKEN=your_bot_token
If you don't have an API key, create one from:
https://rapidapi.com/mynibir/api/free-fire-like1

Then add it to your .env:

ini
Copy
Edit
RAPIDAPI_KEY=your_api_key_from_rapidapi
🌐 Custom or Public API
✅ Option 1: Use RapidAPI
Go to Free Fire Like API on RapidAPI.

Subscribe and get your API key.

Paste it in your .env file:

ini
Copy
Edit
RAPIDAPI_KEY=your_key_here
✅ Option 2: Use Your Own API
Host your own version of the API: Free Fire Like API

In the bot code (cogs/likeCommands.py), replace:

python
Copy
Edit
self.api_host = "https://free-fire-like1.p.rapidapi.com"
with:

python
Copy
Edit
self.api_host = "http://localhost:5000"  # or your public server URL
Leave RAPIDAPI_KEY empty in .env:

ini
Copy
Edit
RAPIDAPI_KEY=



🛠 Technologies Used
Python

Discord.py

Flask

dotenv

aiohttp

📄 License
This project is licensed under the MIT License. Feel free to use and modify it.

👨‍💻 Author
Nibir
