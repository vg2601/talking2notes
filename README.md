# 🎙️ talking2notes (Project Blueprint)

This repository serves as the official placeholder and technical specification for the **talking2notes** AI tool.

## 🔗 Private Project Context
> [!IMPORTANT]
> **ACCESS RESTRICTED:** The link below contains the logic and development history of this project. It is only accessible to the account owner.
> 
> [👉 RESUME CHAT WITH GEMINI HERE](https://gemini.google.com/u/2/app/754425050846ab79)

---

## 🛠️ Phase 1: Technical Architecture
These are the finalized specs for the build:

### 1. The Dashboard (User Interface)
- **Batch Processing:** Users can upload multiple files in one go.
- **Grid Entry:** Uses `ipywidgets` to create a table where each file has a unique **Start Time** and **End Time** input.
- **Sequential Execution:** The AI will process files one-by-one to manage Colab's RAM.

### 2. The AI Engine
- **Slicing:** Uses `pydub` to trim audio *before* transcription to save processing time.
- **Diarization:** Pyannote 3.1 for speaker identification (Who said what).
- **Transcription:** OpenAI Whisper (Turbo) for high-accuracy Hindi/English text.

### 3. Integration
- **Obsidian:** Auto-formatted `.md` files with timestamps.
- **Reports:** Professional `.pdf` summaries generated via `markdown-pdf`.

---

## 📋 Pre-Flight Checklist (For Next Session)
- [ ] Create `requirements.txt` with `pydub`, `ipywidgets`, and `pyannote`.
- [ ] Implement the `run_transcription_pipeline` function in `src/transcribe.py`.
- [ ] Finalize the interactive UI in `notebooks/app.ipynb`.
- [ ] Ensure Hugging Face tokens are generated and model terms are accepted.
