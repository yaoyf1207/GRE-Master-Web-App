# 🎓 GRE Verbal Master (2025 Edition)

<!-- 替换下面的链接为你真实的 Vercel 链接 -->
> **Live Demo:** [https://gre-god-help-3zfv2bp8l-yifans-projects-5baccfbb.vercel.app/](https://gre-god-help-3zfv2bp8l-yifans-projects-5baccfbb.vercel.app/)

![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen)
![Tech Stack](https://img.shields.io/badge/Vue.js-3.0-42b883)
![Style](https://img.shields.io/badge/Tailwind-CSS-38bdf8)
![Deployment](https://img.shields.io/badge/Vercel-Deployed-black)

**GRE Verbal Master** is a lightweight, offline-first Progressive Web App (PWA) engineered to optimize vocabulary acquisition for the GRE General Test. It bridges the gap between static word lists and interactive, contextual learning.

---

## Project Background

**The Problem:** Traditional vocabulary apps lack flexibility in data import (custom Excel sheets) and fail to provide contextual usage for specific word pairs (Sentence Equivalence).

**The Solution:** A custom-built SPA (Single Page Application) that combines **Heuristic Data Parsing** with **Generative AI** to create a personalized, immersive learning experience.

---

## Key Features

### 1. Intelligent Excel Import 
Unlike standard importers that require strict templates, this app uses a **Heuristic Parsing Algorithm**:
- **Automatic Semantic Detection**: Scans rows to detect Chinese characters (`[\u4e00-\u9fa5]`) and automatically maps them as the "Meaning" column.
- **Structure Recognition**: Identifies the first English column as the "Target Word" and merges remaining columns as "Synonyms".
- **Powered by**: `SheetJS` for robust file handling.

### 2. AI-Driven Contextual Learning
- **Generative Mnemonics**: Integrates with LLMs (OpenAI/DeepSeek) to generate vivid short stories using the exact words you are currently studying.
- **Customizable Themes**: Users can instruct the AI to write in specific styles (e.g., *"Sitcom style"*, *"Sci-Fi"*, *"Harry Potter universe"*).
- **History Log**: All generated stories are saved locally with timestamps, allowing for review and context reinforcement.

### 3. Interactive Dashboard & Analytics
- **Visual Progress Tracking**: Real-time progress bars for multiple word lists simultaneously.
- **Daily Goals**: Tracks daily words learned (auto-resets at midnight).
- **Granular Control**: Reset progress for specific days/lists or wipe data individually.

### 4. Immersive Flashcard System
- **3D Flip Animations**: Smooth, hardware-accelerated transitions.
- **Favorites System**: One-click star mechanism to curate a "Review List" for difficult words.
- **Session Management**: Displays word indexing (`# 5 / 60`) for better pacing.

---

## Technical Architecture

This project follows a **Serverless, Client-Side First** architecture to ensure privacy and speed.

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend Framework** | **Vue.js 3** | Composition API for reactive state management. |
| **Styling** | **Tailwind CSS** | Utility-first CSS for responsive, modern UI. |
| **Data Persistence** | **LocalStorage API** | Stores progress, settings, and histories locally in the browser. |
| **File Processing** | **SheetJS (XLSX)** | Client-side parsing of user-uploaded Excel files. |
| **AI Integration** | **RESTful API** | Direct calls to LLM endpoints (BYOK pattern). |
| **CI/CD** | **GitHub + Vercel** | Automated deployment pipeline. |

---

## Security & Privacy (BYOK)

This application adopts the **Bring Your Own Key (BYOK)** security model:
1.  **Client-Side Execution**: All logic runs within the user's browser. No backend server is maintained.
2.  **Local Storage**: API Keys are stored in the browser's `localStorage` sandbox and are never transmitted to the developer or third parties.
3.  **Direct Communication**: API requests are sent directly from the client to the OpenAI/Provider endpoints.

---

## How to Run Locally

Since this is a portable Single-File Application, no complex build environment (`npm`/`node`) is strictly required for usage.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/gre-verbal-master.git
    ```
2.  **Run:**
    Simply open the `index.html` file in Chrome, Edge, or Safari.

---

## License

This project is open source and available under the [MIT License](LICENSE).

---

> *Developed by [Your Name] as a Portfolio Project.*
