# Saarthi (सारथी) – Private AI Study Buddy

An AI study assistant that runs **entirely in your browser** using open-source language models. Paste a chapter, or upload a **PDF, Word (.docx), image (photo of notes, read with OCR) or text file**, and get a summary, a simple explanation, an interactive quiz, flashcards, or answers to your questions in English.

## Why it's different
- **Private:** notes never leave the device (no server, no API calls with your data).
- **Free & offline-capable:** no API key. After the first download, the model is cached and works without internet.
- **Open source & tiny:** LaMini-Flan-T5 77M (about 80 MB), run with [Transformers.js](https://github.com/xenova/transformers.js). No GPU needed.
- **Inclusive:** built for students with low or unreliable internet, and works for any English study material.

## Run it
1. Use any modern browser (Chrome or Edge recommended).
2. Run a tiny local server (browsers block ES modules on some `file://` setups):
   ```
   python -m http.server 8000
   ```
   then open http://localhost:8000
3. Click **Load model**, paste notes (or click *Try sample*), choose a mode.

## Deploy free (for judges)
- **GitHub Pages:** push `index.html` to a repo → Settings → Pages → deploy from `main`.
- or drag the folder onto **Netlify Drop** / **Vercel**.

## Tech
Single-file HTML + JavaScript. File reading is also done locally in the browser with pdf.js (PDF), mammoth.js (.docx) and Tesseract.js (image OCR). Transformers.js runs the quantised LaMini-Flan-T5 model in the browser (WebAssembly). Quiz and flashcards are built from question/answer pairs the model writes for each part of your notes.

## 60-second pitch idea
1. **Problem:** Good AI tutors need paid APIs and constant internet; many students have neither, and privacy is a worry.
2. **Solution:** Saarthi puts an open-source AI tutor inside the browser.
3. **Demo:** Load model → paste a chapter → summary → quiz → flashcards.
4. **Impact:** Free, private, offline, works for any subject.

## Ideas to extend (if you have time)
- PDF upload (pdf.js), voice input/output (Web Speech API), saved progress in localStorage, more languages.
