

# 🚫 Instagram Blocker

An automation tool built with Flask + Selenium that helps users log in to Instagram, fetch their direct messages, and generate a block list of specific friends or accounts automatically.

This project can be extended for:

Monitoring Instagram DMs

Filtering/blocking unwanted users

Automating certain Instagram workflows


**✨ Features**

 🔑 User Login Automation via Selenium WebDriver

 📩 Scrapes Instagram Direct Messages from inbox

 🛡️ Generates Block List of specific accounts

 ⚡ Flask Web Interface with endpoints for login & block list display

 🗃️ (Optional) SQLite integration (SQLAlchemy ORM) to store chat history
 

**🛠️ Tech Stack**

Backend Framework: Flask (Python)

Automation: Selenium, WebDriver Manager (Chrome)

Database (Optional): SQLite with SQLAlchemy ORM

Frontend: HTML (templates with Flask Jinja2)


**📂 Project Structure**

instagram-blocker/

│── app.py              # Flask application with routes

│── scraper.py          # Custom scraper logic for messages

│── templates/

│   ├── index.html      # Login page

│   ├── block_list.html # Block list display

│── requirements.txt    # Python dependencies

│── README.md           # Documentation


**⚡ Getting Started**

 1️⃣ Clone the Repository
git clone https://github.com/Kusuma431/Insta_blocker.git
cd instagram-blocker

 2️⃣ Install Dependencies

It’s recommended to use a virtual environment:

python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows


Install requirements:

pip install -r requirements.txt

 3️⃣ Run the Flask App
python app.py


App runs on 👉 http://127.0.0.1:5000/


**⚙️ Usage**

Open the app in your browser.

Enter your Instagram username & password.

Provide a list of usernames (friends) you want to monitor/block.

The tool will:

Log in to Instagram

Navigate to your DMs

Scrape conversations

Display a block list on the /block-list page


**⚠️ Important Notes**

🔒 Security Warning: Don’t use your main Instagram account for testing—Instagram may temporarily lock accounts for automation.

🕒 Use with caution: frequent logins via Selenium might trigger Instagram’s rate limiting / bot detection.

📌 For production use, you should:

Encrypt credentials

Use session storage instead of raw login each time

Handle Instagram API (official) if possible


**💡 Future Improvements**

✅ Add SQLite Database Storage for scraped messages

✅ Implement automatic block action instead of just generating block list

✅ Multi-account support

✅ Dockerize the app for easy deployment
