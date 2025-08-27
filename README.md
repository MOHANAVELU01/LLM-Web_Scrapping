# Reddit-User-Persona-Generation-using-LLMs-and-Web-Scraping

## 📌 Overview

This project automates the process of generating **user personas** from Reddit profiles by combining **web scraping** with **Large Language Models (LLMs)**. The system collects a user’s Reddit activity (posts and comments), structures the data, and then feeds it to an LLM to produce a detailed persona with insights such as demographics, interests, behavior patterns, and personality traits.

## 🎯 Objectives

* Scrape Reddit user activity (posts & comments).
* Structure the scraped data into a clean format.
* Use an LLM (Gemini 2.0 Flash in this case) to generate a **comprehensive persona report**.
* Save the output to a readable text file for further analysis.

## 🛠️ Tech Stack

* **Python 3.8+**
* **Selenium** – for automated Reddit profile scraping.
* **BeautifulSoup4** – for parsing scraped HTML.
* **Google Generative AI (Gemini 2.0 Flash)** – for persona generation.
* **webdriver-manager** – for handling ChromeDriver setup.

## 📂 Project Structure

```
├── main.py                   # Main script for scraping & persona generation
├── Output_kojied_persona.txt # Example generated persona
├── README.md                 # Project documentation
```

## ⚙️ Installation & Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/Reddit-User-Persona-Generation-using-LLMs-and-Web-Scraping.git
   cd Reddit-User-Persona-Generation-using-LLMs-and-Web-Scraping
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   *(If `requirements.txt` is missing, install manually:)*

   ```bash
   pip install selenium beautifulsoup4 webdriver-manager google-generativeai
   ```

3. Ensure you have **Google API Key** for Gemini. Replace the placeholder in `main.py`:

   ```python
   GOOGLE_API_KEY = "your_api_key_here"
   ```

4. Make sure **Google Chrome** is installed on your system.

## 🚀 Usage

1. Run the script:

   ```bash
   python main.py
   ```

2. Enter a Reddit profile URL when prompted:

   ```
   Enter Reddit profile URL: https://www.reddit.com/user/kojied/
   ```

3. The program will:

   * Scrape posts and comments.
   * Save structured data to `<username>_data.txt`.
   * Generate a persona report using Gemini.
   * Save the final persona to `<username>_persona.txt`.

4. Example output file:
   [`Output_kojied_persona.txt`](./Output_kojied_persona.txt)

## 📑 Example Persona Output

The generated persona includes:

* **Demographics** (age, location, profession, political stance)
* **Interests** (technology, finance, gaming, gardening, etc.)
* **Behavior Patterns** (advice-seeking, speculative discussions, problem-solving)
* **Personality Traits** (curious, analytical, humorous, future-oriented)
* **Other Observations** (style of communication, Reddit conventions)

*(See [`Output_kojied_persona.txt`](./Output_kojied_persona.txt) for full example.)*

## 🛡️ Error Handling

* Gracefully handles:

  * Invalid Reddit usernames/URLs.
  * Empty or restricted profiles.
  * Reddit downtime or blocked requests.

## 📌 Future Improvements

* Support for pagination (fetching more posts).
* Docker containerization for easy deployment.
* Unit tests & CI workflows.
* Support for other LLMs (OpenAI GPT, Claude, etc.).

