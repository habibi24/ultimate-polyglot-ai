# **Ultimate Polyglot AI — Context Reader Pro**

A cutting-edge Single-Page Application (SPA) for immersive language learning. Built with HTML5, Vanilla JS, and the Gemini API — engineered to simulate real-world conversations, provide granular phonetic feedback, and dynamically adapt to the user's proficiency level (CEFR A1-C2).

Powers real-time speech evaluation, emotion-driven Text-to-Speech (TTS), hidden spaced repetition (Flashback), and procedural ambient audio — all served purely from the client side without relying on heavy frameworks.

## **Architecture**

  User Client                                     Cloud Services  
       |                                                |  
       |  Mic Input (Web Speech API)                    |  
       |  Text Prompt                                   |  
       v                                                v  
  \+-----------------------+                    \+-----------------------+  
  |  Browser Engine       | \--- JSON Payload \-\>|  Google Gemini API    |  
  |  (index.html)         | \<- TTS / JSON Data |  (gemini-2.5-flash)   |  
  \+-----------------------+                    \+-----------------------+  
       |  
       \+---\> UI Rendering (Tailwind CSS, DOM Manipulation)  
       \+---\> Pronunciation Analysis (Color-coded scaffolding)  
       \+---\> Audio Playback (Web Audio API Procedural Sound)  
       \+---\> Persistence (IndexedDB for Audio, LocalStorage for JSON)

Data flow: The user inputs a prompt or uses the microphone. The browser sends a strictly structured JSON generation request to the **Gemini API**. Gemini returns the conversational script, emotion cues, and translations. If Cloud Voice is enabled, the app fetches **Gemini Neural TTS** audio blobs and caches them in **IndexedDB** for zero-latency playback. The **Web Speech API** listens to the user's reading and matches it against the generated transcript for granular, real-time visual feedback.

## **Tech Stack**

| Layer | Technology |
| :---- | :---- |
| **Frontend UI** | HTML5, CSS3, Tailwind CSS (via CDN) |
| **Core Logic** | Vanilla JavaScript (ES6+) |
| **AI Framework** | Google Gemini API (gemini-2.5-flash-preview) |
| **Speech Recognition** | Web Speech API (SpeechRecognition) |
| **Voice Synthesis** | Gemini Neural TTS, SpeechSynthesisUtterance |
| **Audio Processing** | Web Audio API (Procedural Ambient Sound Generation) |
| **Data Persistence** | Browser LocalStorage, IndexedDB (Audio Blob Caching) |

## **Installation & Setup**

**1\. Clone the repository**

git clone \[https://github.com/your-username/ultimate-polyglot-ai.git\](https://github.com/your-username/ultimate-polyglot-ai.git)  
cd ultimate-polyglot-ai

**2\. Configure API Key**

Open index.html using your preferred code editor. Locate the API variable near the bottom of the script and set your Gemini API key:

// Replace with your actual Google AI Studio API Key  
const apiKey \= "INSERT\_YOUR\_GEMINI\_API\_KEY\_HERE";

**3\. Run the application**

Since this is a fully client-side Single-Page Application, there is no need to spin up a server, Node.js, or Docker. Simply open the file in your browser:

\# On macOS  
open index.html

\# On Windows  
start index.html

\# Or simply double-click index.html in your File Explorer

**Note:** For the best Speech-to-Text (Microphone) experience, it is highly recommended to run this application on **Google Chrome**.

## **Screenshots**

Here is a preview of the **Interactive Deep Contextual Analysis** feature, powered by our AI ✨:

## **Core Features**

* **Adaptive AI Scenario Generator:** Dynamically adjusts vocabulary and grammar to the user's CEFR Level (A1-C2) and scene mood. Guarantees 100% unique stories with randomized Micro-Context injections to prevent AI laziness.  
* **Interactive Pronunciation Scaffolding:** Evaluates speech in real-time with visual indicators:  
  * 🟩 **Green:** Correct pronunciation.  
  * 〰️ **Orange Wavy:** Extra or mispronounced word.  
  * ⬜ **Gray Strikethrough:** Missed target word.  
* **Minimal Pair Protection System:** Detects vowel pronunciation shifts (e.g., *sheet* vs *ship*) and provides educational phonetic warnings.  
* **Hidden Spaced Repetition (Flashback):** Missed words are stored locally and reappear naturally in future AI-generated dialogues to improve long-term memory.  
* **Live Call AI & Roleplay:** Features a "Smart Wait" system where the AI initiates conversation if the user is silent, alongside interactive turn-taking simulations.  
* **Gen-Z Slang Translation:** Converts stiff formal dialogues into casual Indonesian street slang (e.g., "I'm broke" → "Gue lagi bokek").

## **The Origin Story & Inspiration**

The idea behind Ultimate Polyglot AI was inspired by personal experiences with language exposure through entertainment media.

Growing up, I often watched older animated shows and television programs that featured simple English subtitles and conversational dialogue. Repeated exposure to those conversations gradually helped build natural familiarity with vocabulary and sentence structures. Another major influence came from listening to songs from different languages and cultures. These experiences highlighted how emotional context, repetition, immersion, and entertainment can make language learning feel more natural and memorable.

Those experiences became the foundation of Ultimate Polyglot AI — an attempt to combine immersive storytelling, AI-driven interaction, pronunciation training, and emotional engagement into a modern adaptive language learning experience.

### **🎓 Built on a Solid AI Foundation**

The advanced prompt engineering and AI architectural design behind this application were made possible by the foundational knowledge acquired from the **Career Essentials in Generative AI by Microsoft and LinkedIn** certification (Completed by S.M. Hasyim on May 15, 2026). The principles learned from this pathway allowed us to push the Gemini API to its absolute limits.

## **Engineering Challenges**

Developing this application involved solving several unique linguistic and technical hurdles:

1. **The Tragedy of the "Robot Voice":** Initially, the AI's TTS sounded stiff. We implemented *Native Emotion Injection* prompting to force the AI to change its "vocal cords," ensuring it sounded like a native speaker with raw emotions.  
2. **The War Against "AI Laziness":** Generative AI often defaults to repetitive scenarios. To break this *Template Syndrome*, we pushed the AI's temperature to extreme levels (1.7) and injected forced, hidden *Plot Twists*.  
3. **The Live Call Delay Mystery:** Early versions of the *Live Call* suffered from severe latency (*Racing Condition*). We solved this by engineering a *Smart Wait* state machine and *Abort Controllers* for seamless turn-taking.

## **Future Roadmap**

* \[ \] Multi-language support (Japanese JLPT, Mandarin HSK mappings).  
* \[ \] Progressive Web App (PWA) integration for native-like mobile installation.  
* \[ \] Gamification elements (Daily Streaks, XP system).  
* \[ \] OpenAI Whisper API integration for phoneme-level pronunciation scoring.

## **Author**

Developed by **S.M. Hasyim**.

## **License**

This project was developed for educational and portfolio purposes.