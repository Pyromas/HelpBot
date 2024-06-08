Project Management Database with Telegram Bot
Overview
This project is a database management system designed to handle projects and their associated skills and statuses. The system is implemented using SQLite and Python, and includes a Telegram bot interface to manage projects interactively.

Table of Contents
Overview
Installation
Usage
Initialization
Telegram Bot Commands
Inserting Data
Querying Data
Updating Data
Deleting Data
Project Structure
Contributing
License
Installation
Clone the repository:

bash
Копировать код
git clone https://github.com/yourusername/project-management-db.git
cd project-management-db
Create a virtual environment and activate it:

bash
Копировать код
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install the required packages:

bash
Копировать код
pip install -r requirements.txt
Configure the database:
Ensure that the config.py file contains the correct path to your SQLite database:

python
Копировать код
DATABASE = 'path_to_your_database.db'
Configure the Telegram Bot:
Ensure that the logic.py file contains the correct token for your Telegram bot:

python
Копировать код
bot = TeleBot('YOUR_TELEGRAM_BOT_TOKEN')
Usage
Initialization
To initialize the database with the required tables and insert default values for skills and statuses, run the following commands:

python
Копировать код
from logic import DB_Manager
from config import DATABASE

manager = DB_Manager(DATABASE)
manager.create_tables()
manager.default_insert()
Telegram Bot Commands
The bot provides the following commands:

/start - Start the bot and display a welcome message.
/info - Display a list of available commands.
/new_project - Add a new project.
/projects - Display all projects.
/update_projects - Update project information.
/skills - Assign skills to a project.
/delete - Delete a project.
Inserting Data
To insert a new project, use the /new_project command in the Telegram bot and follow the prompts.

Querying Data
To get the list of all projects for a specific user, use the /projects command in the Telegram bot.

To get the skills associated with a project, simply send the project name as a message to the bot.

Updating Data
To update a project's attribute, use the /update_projects command in the Telegram bot and follow the prompts.

Deleting Data
To delete a project, use the /delete command in the Telegram bot and follow the prompts.

Project Structure
bash
Копировать код
project-management-db/
│
├── logic.py                # Database manager and Telegram bot logic
├── config.py               # Configuration file with database path and bot token
├── requirements.txt        # Python package requirements
└── README.md               # This README file
Contributing
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes.
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-branch).
Create a new Pull Request.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Теперь ваш README файл включает все необходимые инструкции для работы с базой данных и Telegram ботом, что облегчает пользователям понимание и использование проекта.
