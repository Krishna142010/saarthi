# Saarthi (सारथी) – Private AI Study Buddy

An AI study assistant that runs **entirely in your browser** using open-source language models. Paste a chapter and get a summary, a simple explanation, an interactive quiz, flashcards, or answers to your questions in English, Hindi or Hinglish.

## Why it's different
- **Private:** notes never leave the device (no server, no API calls with your data).
- **Free & offline-capable:** no API key. After the first download, the model is cached and works without internet.
- **Open source:** Llama 3.2 (Meta), Qwen 2.5 (Alibaba), Gemma 2 (Google), via [WebLLM](https://github.com/mlc-ai/web-llm) and WebGPU.
- **Inclusive:** built for students with low or unreliable internet, with Hindi/Hinglish support.

## Run it
1. Use the latest **Chrome or Edge** (WebGPU needed).
2. Run a tiny local server (browsers block WebGPU modules from some `file://` setups):
   ```
   python -m http.server 8000
   ```
   then open http://localhost:8000
3. Click **Load model**, paste notes (or click *Try sample*), choose a mode.

## Deploy free (for judges)
- **GitHub Pages:** push `index.html` to a repo → Settings → Pages → deploy from `main`.
- or drag the folder onto **Netlify Drop** / **Vercel**.

## Tech
Single-file HTML + JavaScript. `@mlc-ai/web-llm` runs quantised open models on the GPU through WebGPU. Quiz and flashcards are generated with structured prompts and parsed on the client.

## 60-second pitch idea
1. **Problem:** Good AI tutors need paid APIs and constant internet; many students have neither, and privacy is a worry.
2. **Solution:** Saarthi puts an open-source AI tutor inside the browser.
3. **Demo:** Load model → paste a chapter → summary → quiz → switch to Hindi.
4. **Impact:** Free, private, offline, works for any subject.

## Ideas to extend (if you have time)
- PDF upload (pdf.js), voice input/output (Web Speech API), saved progress in localStorage, more languages.
