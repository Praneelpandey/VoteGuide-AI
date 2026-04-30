# VoteGuide AI 🗳️

### Challenge Vertical: Election Process Assistant

An interactive, AI-powered single-page web application that helps Indian voters understand the complete election process — from announcement to oath-taking.

---

## Approach & Logic

VoteGuide AI combines three strategies for a reliable and engaging experience:

1. **Google Gemini AI for Dynamic Q&A** — The Gemini 2.0 Flash model powers the chat assistant, enabling natural language conversations about any election topic. Users can ask in English, Hindi, or other languages.

2. **Hardcoded Knowledge Base for Reliability** — Critical election data (6 timeline steps, key facts, security deposit amounts, deadlines) is embedded directly in the app. This ensures accurate information is always available, even before the AI responds.

3. **Interactive Timeline for Visual Learning** — A vertical stepper breaks the election process into 6 clear stages. Each step expands to reveal descriptions, key facts, and an "Ask AI about this →" button — bridging static content with dynamic AI exploration.

---

## How It Works

```
User opens app → Sees "Did You Know?" fact ticker rotating election trivia
                → Browses the 6-step Election Timeline (left panel)
                → Clicks a step to expand details + key facts
                → Clicks "Ask AI about this →" to get a detailed AI explanation
                → OR picks a Quick Question pill button (right panel)
                → OR types a custom question in the chat
                → Gemini AI responds with concise, factual answers
                → Timeline highlights the relevant step
```

### Key User Flows:
- **Explore Mode**: Click timeline steps → read hardcoded facts → dive deeper with AI
- **Ask Mode**: Type or select a question → get instant AI-powered answers
- **Learn Mode**: Read the rotating "Did You Know?" facts while browsing

---

## Google Services Used

| Service | Purpose |
|---------|---------|
| **Google Gemini API** (`gemini-2.0-flash`) | Core AI engine — powers the conversational chat assistant with election expertise |
| **Google Fonts** (`Rajdhani`, `Noto Sans`) | Typography — Rajdhani for bold civic headings, Noto Sans for readable body text |

---

## Features

- 💬 **AI Chat Assistant** — Ask anything about Indian elections in natural language
- 📋 **Interactive Timeline** — 6-step expandable stepper with key facts and "Ask AI" buttons
- ⚡ **Quick Question Buttons** — 8 pre-loaded common voter queries
- 💡 **Fact Ticker** — Rotating "Did You Know?" bar with 5 election facts (auto-rotates every 4s)
- 🌐 **Multilingual Support** — The AI responds in whatever language you write in
- 📱 **Fully Responsive** — Works on desktop (3-panel) and mobile (drawer navigation)
- 🔑 **Secure API Key Handling** — Key stored in browser localStorage only, never transmitted to third parties

---

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/VoteGuide-AI.git
   cd VoteGuide-AI
   ```

2. **Get a free Gemini API key**
   - Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Click "Create API Key" and copy it

3. **Add your API key** (choose one method)
   - **Option A (in-app):** Open the app and paste your key in the modal that appears
   - **Option B (in code):** Replace `YOUR_API_KEY_HERE` in `index.html` line ~198

4. **Open in browser**
   ```bash
   # Simply open the file directly
   open index.html
   
   # Or serve locally
   python -m http.server 8080
   # Then visit http://localhost:8080
   ```

---

## Tech Stack

- **Frontend:** Pure HTML5 + CSS3 + ES6+ JavaScript (single file, no build tools)
- **AI:** Google Gemini API (REST, `v1beta` endpoint)
- **Fonts:** Google Fonts (Rajdhani, Noto Sans)
- **No dependencies:** No npm, no frameworks, no build step — just open and go

---

## Project Structure

```
VoteGuide-AI/
├── index.html    ← Complete app (HTML + CSS + JS, all inline)
├── README.md     ← This file
└── .gitignore    ← Git ignore rules
```

---

## Assumptions

- Focused on the **Indian general election process** (Lok Sabha / State Assembly)
- Requires an **internet connection** for Gemini API calls and Google Fonts
- Works in **any modern browser** (Chrome, Firefox, Edge, Safari) without installation
- API key is the user's responsibility — free tier has rate limits
- All hardcoded election data is based on current ECI guidelines

---

## Disclaimer

This tool is for **educational purposes only**. Always refer to the [Election Commission of India](https://eci.gov.in/) for official and up-to-date information.

---

**Built for Google Promptwars Hackathon** · Powered by Gemini AI
