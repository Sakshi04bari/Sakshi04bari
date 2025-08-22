import os
import sys

# Load API key from environment
MISTRAL_API_KEY = os.getenv("MISTRAL_API_KEY")

if not MISTRAL_API_KEY:
    skills = [
        "Python 🐍", "Core Java ☕", "Flask 🌐", "REST API ⚡",
        "HTML/CSS 🎨", "SQL 🗄️", "MongoDB 🍃", "LLMs 🤖"
    ]

    error_message = f"""
    ❌ ERROR: MISTRAL_API_KEY not found!  

    👉 Please set it in your environment before running the app.

    Example:
        On Windows PowerShell:
            $env:MISTRAL_API_KEY="your_api_key_here"
        On Linux/Mac:
            export MISTRAL_API_KEY="your_api_key_here"

    💡 Developer Skills:
        {", ".join(skills)}

    🚀 Pro Tip: Store your keys securely using a .env file with `python-dotenv`.
    """

    sys.exit(error_message)
