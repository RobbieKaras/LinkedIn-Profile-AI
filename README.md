# LinkedIn Profile Coach AI

An AI-powered tool that analyzes LinkedIn profiles and helps users improve how they present themselves professionally. Built for students and early-career professionals who want to stand out.

---

## About

Many students and early-career professionals struggle with presenting their experience clearly, structuring their LinkedIn profile effectively, and knowing what skills or certifications to add. This tool bridges that gap by acting as a **LinkedIn profile coach powered by AI**.

---

## Features

### Profile Analysis
Analyzes your LinkedIn profile and generates a structured report covering:
- Headline quality
- About section effectiveness
- Experience improvement suggestions
- Skills and certifications recommendations
- Featured section ideas
- Banner / visual branding feedback
- Overall profile completeness score

### Step-by-Step Improvement Plan
Generates a clear, prioritized action plan — for example:
1. Rewrite your headline to reflect your target role
2. Add a compelling About section
3. Expand experience descriptions with measurable impact

### Career-Specific Suggestions
Detects your likely career focus and surfaces relevant recommendations, including LinkedIn Learning certifications, key technical skills, and portfolio or project ideas. Supported areas include:
- Cybersecurity
- Software Engineering
- Data Science
- Business Analytics
- Marketing

### Improved Profile Generator
Automatically rewrites your:
- Headline
- About section
- Experience descriptions
- Featured section
- Skills list
- Banner suggestion with a ready-to-use AI image generation prompt

Generated content can be copied directly into LinkedIn.

### AI Chat Assistant
An interactive coach for follow-up questions after your analysis. Example questions:
- *How can I improve my experience section?*
- *What cybersecurity certifications should I add?*
- *How should I present my projects?*

### Resume Integration *(optional)*
Paste your resume alongside your LinkedIn data to improve analysis accuracy. The AI will cross-reference both to surface missing skills, additional experience details, and projects worth showcasing.

### LinkedIn Data Export Support
For the most accurate results, import your LinkedIn data archive instead of copying text manually. The tool reads your exported CSV files automatically (see [Recommended Workflow](#recommended-workflow-start-here) below).

### Saved Reports & Cached Profiles
- Generated reports are saved as `.md` files to the `output/` folder with timestamped filenames (e.g. `linkedin_profile_report_2025-03-12_14-30-00.md`)
- Your last profile input is cached in `cache/` so you don't need to re-paste it on every run

---

## Recommended Workflow *(Start Here)*

Using your LinkedIn data export produces significantly better results than pasting text manually.

### Step 1 — Download Your LinkedIn Data
Go to LinkedIn → **Settings & Privacy → Data Privacy → Get a copy of your data**, then select **Download larger data archive**. LinkedIn will email you a ZIP file.

### Step 2 — Extract the Archive
Right-click the ZIP → **Extract All**. Inside, you should see files like:
```
Profile.csv
Positions.csv
Education.csv
Skills.csv
```

### Step 3 — Run the Program in VS Code

Open the project in VS Code, launch a terminal (**Terminal → New Terminal**), and run:

```bash
python main.py
```

When prompted, choose option `2) Use LinkedIn data export folder` and paste the path to your extracted folder:

```
C:\Users\YourName\Downloads\LinkedInData
```

> **Prefer a quick start?** You can choose option `1) Paste LinkedIn profile text` instead — just note that the export method gives more complete results.

---

## Installation & Setup

### 1. Prerequisites

Install the following if you haven't already:
- [Python 3.10+](https://www.python.org/downloads/) — make sure to check **Add Python to PATH** during installation
- [Visual Studio Code](https://code.visualstudio.com/) *(recommended)*

Verify Python is installed:
```bash
python --version
```

### 2. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/LinkedIn-Profile-AI.git
cd LinkedIn-Profile-AI
```

Or download the ZIP from GitHub: **Code → Download ZIP**, then extract it.

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Your API Key

This project uses a `.env` file to securely store your Gemini API key.

Rename the example file:
```
.env.example  →  .env
```

Then open `.env` and add your key:
```env
GEMINI_API_KEY=your_api_key_here
GEMINI_MODEL=gemini-2.5-flash
```

Get a free Gemini API key at [https://ai.google.dev](https://ai.google.dev).

### 5. Run the Program

```bash
python main.py
```

Follow the prompts to select your input method, optionally add your resume, and generate your analysis.

---

## Example Workflow

```
Run program
    ↓
Choose input method
    1) Paste LinkedIn text
    2) LinkedIn data export folder
    ↓
(Optional) Paste resume text
    ↓
AI analyzes your profile
    ↓
Receive full report + improvement plan
    ↓
Choose next action:
    - Generate rewritten sections
    - Chat with AI coach
    - Save report
```

---

## Project Structure

```
LinkedIn-Profile-AI/
│
├── main.py
├── requirements.txt
├── README.md
├── .env.example
│
├── src/
│   ├── analyzer.py
│   ├── gemini_client.py
│   ├── linkedin_parser.py
│   ├── post_analysis.py
│   └── report_generator.py
│
├── output/          # Generated reports saved here
└── cache/           # Cached profile data
```

---

## Technologies Used

- Python
- Google Gemini API
- CSV parsing
- CLI interface
- Prompt engineering

---

## Planned Features

- GUI interface
- Resume file upload (PDF/DOCX)
- Profile comparison mode
- LinkedIn banner generator
- Web application deployment

---

## License

MIT License

---

## Author

**Robbie Karas**  
Computer Information Systems student at James Madison University  
Interests: Cybersecurity, AI tools, and practical automation projects
