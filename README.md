# Selenium to Playwright Converter (Local LLM)

A web-based tool to convert **Selenium Java (TestNG)** code into **Playwright TypeScript (Page Object Model)** using a local **Ollama (Codellama)** instance.

## 🚀 Features

- **Local Processing**: Uses Ollama running locally for privacy and no API costs.
- **Strict POM**: Enforces Page Object Model separation in the output.
- **Modern UI**: React-based interface with Monaco Editor for code viewing/editing.
- **Multi-file Output**: Automatically splits logic into Page Objects and Test Specs.

## 🛠️ Prerequisites

1.  **Node.js** (v18+ or v20+ recommended, v22.4.0 verified compatible)
2.  **Ollama** running locally on port `11434`.
3.  **Codellama Model** pulled: `ollama pull codellama`

## 🏃‍♂️ How to Run

### 1. Start the Backend (Conversion Server)
```bash
# In the root directory
node server/index.js
# Runs on http://localhost:3001
```

### 2. Start the Frontend (UI)
```bash
# In another terminal, navigate to client/
cd client
npm run dev
# Runs on http://localhost:5173
```

## 🔒 Verification
Open your browser to: **http://localhost:5173**

## 📂 Project Structure
- `server/`: Express.js backend for Ollama communication.
- `client/`: React + Vite frontend.
- `tools/`: Utility scripts (e.g., `check_ollama.js`).
- `architecture/`: Technical documentation/SOPs.
