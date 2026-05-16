<div align="center">

# 🌐 Ultimate Polyglot AI — Context Reader Pro

**Immersive AI-powered language learning. Real conversations. Real pronunciation. Real results.**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Gemini API](https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)

---

<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1ouUv8gFGurSrVziNgeyOlIg436v30ww4" alt="Ultimate Polyglot AI - Main Interface" width="700"/>
  <p><em>Gambar 1: Interface utama menampilkan real-time pronunciation feedback dengan color-coded scaffolding</em></p>
</div>

---

## 🎬 Demo Video

<div align="center">
  <a href="https://www.youtube.com/watch?v=wfeQGhMMRu0">
    <img src="https://img.youtube.com/vi/wfeQGhMMRu0/maxresdefault.jpg" alt="Watch Demo on YouTube" width="700"/>
  </a>
  <p><em>Klik gambar untuk menonton demo lengkap di YouTube</em></p>
</div>

</div>

---

## ✨ What Is This?

**Ultimate Polyglot AI** is a fully client-side Single-Page Application for immersive language learning — no servers, no frameworks, no install required. Powered by the **Gemini 2.5 Flash** API, it simulates real-world conversations, delivers granular phonetic feedback, and dynamically adapts to the learner's CEFR level (A1–C2).

> _Born from the idea that entertainment — cartoons, music, storytelling — is the most natural way to acquire a language._

---

## 🗺️ Architecture

```
  User Client                                      Cloud Services
       │                                                 │
       │  🎤 Mic Input (Web Speech API)                  │
       │  💬 Text Prompt                                  │
       ▼                                                 ▼
  ┌─────────────────────┐                   ┌────────────────────────┐
  │   Browser Engine    │ ── JSON Payload ──▶│   Google Gemini API    │
  │    (index.html)     │ ◀── TTS / JSON ───│  (gemini-2.5-flash)    │
  └─────────────────────┘                   └────────────────────────┘
       │
       ├──▶ 🎨 UI Rendering       (Tailwind CSS, DOM Manipulation)
       ├──▶ 🗣️ Pronunciation Engine (Color-coded Scaffolding)
       ├──▶ 🔊 Audio Playback      (Web Audio API Procedural Sound)
       └──▶ 💾 Persistence         (IndexedDB + LocalStorage)
```

**Data Flow:** User speaks or types → Browser sends a structured JSON request to Gemini → Gemini returns the script, emotion cues, and translations → If Cloud Voice is enabled, Neural TTS audio blobs are fetched and cached in **IndexedDB** for zero-latency playback → **Web Speech API** matches the user's reading to the transcript for real-time visual feedback.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend UI** | HTML5, CSS3, Tailwind CSS (CDN) |
| **Core Logic** | Vanilla JavaScript (ES6+) |
| **AI Engine** | Google Gemini API (`gemini-2.5-flash-preview`) |
| **Speech Recognition** | Web Speech API (`SpeechRecognition`) |
| **Voice Synthesis** | Gemini Neural TTS + `SpeechSynthesisUtterance` |
| **Audio Processing** | Web Audio API (Procedural Ambient Sound) |
| **Data Persistence** | Browser `LocalStorage` + `IndexedDB` (Audio Blob Cache) |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/SMHasyim24/ultimate-polyglot-ai.git
cd ultimate-polyglot-ai
```

### 2. Configure Your API Key

Open `index.html` in your code editor. Near the bottom of the `<script>` block, locate and replace the placeholder:

```javascript
// Replace with your actual Google AI Studio API Key
// Get one free at: https://aistudio.google.com/app/apikey
const apiKey = "INSERT_YOUR_GEMINI_API_KEY_HERE";
```

### 3. Run the App

No server, no Node.js, no Docker — just open the file:

```bash
# macOS
open index.html

# Windows
start index.html

# Linux
xdg-open index.html
```

> 💡 **Tip:** Use **Google Chrome** for the best Speech-to-Text (microphone) experience, as Web Speech API support is most stable there.

---

## 🎯 Core Features

### 🤖 Adaptive AI Scenario Generator
Dynamically adjusts vocabulary and grammar complexity to the user's **CEFR level (A1–C2)** and selected scene mood. Randomized **Micro-Context injections** guarantee 100% unique stories and prevent repetitive AI output.

### 🗣️ Interactive Pronunciation Scaffolding
Evaluates speech in real-time with color-coded visual indicators:

| Indicator | Meaning |
|---|---|
| 🟩 **Green** | Correct pronunciation |
| 🟥 **Red** | Extra or mispronounced word |
| ⬜ **Gray Strikethrough** | Missed target word |

### 🛡️ Minimal Pair Protection System
Detects critical vowel shifts (e.g., *sheet* vs *ship*) and automatically triggers educational phonetic warnings before they become bad habits.

### 🔁 Hidden Spaced Repetition (Flashback)
Missed words are silently stored locally and **reinjected naturally** into future AI-generated dialogues — spaced repetition without the flashcard grind.

### 📞 Live Call AI & Roleplay
Features a **Smart Wait** state machine — if the user goes silent, the AI initiates. Supports full interactive turn-taking simulations for realistic conversational practice.

### 🇮🇩 Gen-Z Slang Translation
Converts stiff formal dialogues into casual **Indonesian street slang**:
> "I'm broke" → **"Gue lagi bokek"**

---

## 📸 Feature Gallery

### Adaptive Scenario Selection
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=17wDVerzsH3tMD5VlD1i5978j9-uA2EsU" alt="Scenario Selection Screen" width="600"/>
  <p><em>Gambar 2: Pilih tingkat kesulitan CEFR (A1-C2), mood scene, dan konteks untuk dialog yang unik dan relevan</em></p>
</div>

### Real-Time Pronunciation Feedback
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1GrKtxE6neruGMnn_pW2zMMbQ0iybTSyj" alt="Pronunciation Feedback" width="600"/>
  <p><em>Gambar 3: Warna-coded scaffolding menunjukkan pengucapan yang benar (hijau), berlebihan (orange wavy), atau terlewat (abu-abu strikethrough)</em></p>
</div>

### Live AI Conversation
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1IlzOrSKoWqCSvZtfh_GTLwfPjSETR5AP" alt="Live Call AI Interface" width="600"/>
  <p><em>Gambar 4: Interactive roleplay dengan Smart Wait system — AI otomatis memulai percakapan jika user diam</em></p>
</div>

### Progress & Flashback Dashboard
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1yTBds4_iXHyu1X85xhqhbPiMvqg1At29" alt="Spaced Repetition Dashboard" width="600"/>
  <p><em>Gambar 5: Track progress pembelajaran</em></p>
</div>

---

## ⚙️ Engineering Challenges

### 🎭 The "Robot Voice" Problem
Early TTS output sounded stiff and unnatural. Solved with **Native Emotion Injection** prompting — forcing the model to adopt emotional vocal cues, making it sound like a native speaker.

### 😴 The "AI Laziness" War
Generative AI defaults to repetitive, templated scenarios. Defeated with extreme **temperature tuning (1.7)** and forced hidden **Plot Twist injections** to break the pattern.

### ⏱️ The Live Call Delay Mystery
Early Live Call suffered severe latency from race conditions. Resolved by engineering a **Smart Wait state machine** paired with **Abort Controllers** for seamless turn-taking.

---

## 🗺️ Roadmap

- [ ] Multi-language support (Japanese JLPT, Mandarin HSK mappings)
- [ ] Progressive Web App (PWA) for native-like mobile installation
- [ ] Gamification: Daily Streaks & XP system
- [ ] OpenAI Whisper API integration for phoneme-level pronunciation scoring

---

## 💡 The Origin Story

The idea behind Ultimate Polyglot AI was born from a simple observation: **entertainment is the most effective language teacher**.

Growing up, exposure to English through animated shows with simple subtitles built vocabulary naturally. Music from different cultures created emotional anchors for unfamiliar words. These experiences proved that immersion, repetition, and emotional engagement make language learning feel effortless.

Ultimate Polyglot AI combines all of that — AI-driven storytelling, pronunciation training, and emotional engagement — into one adaptive modern experience.

> 🎓 The advanced prompt engineering behind this app was built on foundations from the **Career Essentials in Generative AI** certification by Microsoft & LinkedIn — completed by **S.M. Hasyim** on May 15, 2026.

---

## 👤 Author

Developed with passion by **S.M. Hasyim**

---

## 📄 License

This project was developed for **educational and portfolio purposes**.
