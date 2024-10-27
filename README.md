# Deep Questions Discord Bot

A Discord bot designed to engage users with philosophical questions about life, freedom, morality, happiness, and society. This bot provides random deep questions to spark discussions or to provoke thought among users.

## Features
- **Random Deep Questions**: The bot provides thought-provoking questions covering topics like the meaning of life, morality, freedom, happiness, and knowledge.
- **Categorized Questions**: You can request questions from specific categories like "freedom" or "happiness".
- **User Suggestions**: Users can suggest new questions to the bot.
- **Interactive Reaction**: Users can react to get more questions.

## Commands
- `/deep_question [category]`: Get a random deep question. If a category is provided, the question will be from that category.
- `/deep_categories`: List all available categories.
- `/helpbot`: Display help information about the bot's commands.
- `/deep_suggest [suggestion]`: Suggest a new question or idea for the bot.

## Setup and Deployment
### Prerequisites
- Python 3.10 or higher.
- `discord.py` library (v2.3.0).
- Other dependencies as listed in `requirements.txt`.
- A Discord bot token.

### Installation Steps
1. **Clone the repository**
   ```sh
   git clone https://github.com/StLibertos/bot-questions.git
   cd bot-questions
   ```

2. **Create a virtual environment** (recommended)
   ```sh
   python -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```

3. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```

4. **Set the Discord Bot Token**
   You need to set your bot token as an environment variable:
   ```sh
   export DISCORD_BOT_TOKEN="YOUR_BOT_TOKEN"
   ```

5. **Run the bot**
   ```sh
   python deep_questions_bot.py
   ```

### Deployment with Nixpacks
1. **Create a `nixpacks.toml` configuration file**
   Make sure you have `nixpacks.toml` with the following content:
   ```toml
   [phases.setup]
   nixPkgs = ["python310", "pip"]

   [phases.build]
   cmds = ["pip install -r requirements.txt"]

   [start]
   cmd = "python deep_questions_bot.py"
   ```

2. **Add `Procfile`**
   Create a `Procfile` to specify the startup command:
   ```
   web: python deep_questions_bot.py
   ```

### Environment Variables
- `DISCORD_BOT_TOKEN`: Your Discord bot token that is required to connect to the Discord API.

## File Structure
- `deep_questions_bot.py`: Main bot script.
- `requirements.txt`: List of Python dependencies.
- `nixpacks.toml`: Configuration file for deployment.
- `Procfile`: Command to run the bot during deployment.

## Contributing
If you wish to contribute, feel free to submit a pull request or suggest features by creating an issue.

## License
This project is open source and available under the [MIT License](LICENSE).

## Contact
For any questions or suggestions, feel free to contact me through GitHub or Discord.

