# 🎙️ Free Dictation Kit

A free, open-source, offline voice dictation tool for Windows.  
Press and hold **Right Ctrl** → speak → release → text is pasted wherever your cursor is.

No API keys. No subscriptions. No internet required.

---

## ✨ Features

- **System-wide** — works in any application (browser, Word, VS Code, WeChat, etc.)
- **Completely free** — powered by a local Whisper model, no API costs
- **Offline** — no internet connection required after first-time model download
- **Bilingual** — automatic Chinese / English language detection
- **Non-intrusive** — lives in the system tray, out of your way

---

## 🖥️ System Requirements

- Windows 10 or later
- Python 3.9+
- ~500MB disk space (for the Whisper model, downloaded on first run)
- Microphone

> **Note on speed:** On CPU-only machines, transcription takes approximately 5–15 seconds per recording. A dedicated GPU will significantly speed this up.

---

## 🚀 Installation

```bash
# 1. Clone the repository
git clone https://github.com/EdelKevin/Free_Dictation_Kit.git
cd Free_Dictation_Kit

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the app
python main.py
```

> **First launch:** The app will automatically download the Whisper `small` model (~466MB). This only happens once.

---

## 🎤 How to Use

1. Launch the app — a tray icon appears in your taskbar
2. Place your cursor in any text field
3. **Hold Right Ctrl** to start recording (tray icon turns red)
4. Speak in English or Chinese
5. **Release Right Ctrl** — transcription begins (tray icon shows loading)
6. Text is automatically pasted at your cursor position

**If your cursor is not in a text field**, the transcribed text is copied to your clipboard and a notification appears.

---

## 📋 Status Indicators

| Tray Icon State | Meaning |
|-----------------|---------|
| Normal | Idle, ready |
| Red | Recording |
| Animated | Transcribing |

| Notification | Meaning |
|--------------|---------|
| "Text copied to clipboard" | Cursor was not in a text field |
| "Transcription failed" | Network or model error |

---

## 🗺️ Roadmap

**MVP (current)**
- [x] Project structure & documentation
- [ ] Right Ctrl global hotkey
- [ ] Local Whisper transcription (offline)
- [ ] System tray with status indicators
- [ ] Auto-paste via clipboard
- [ ] Toast notifications

**V2 (planned)**
- [ ] LLM-based text polishing
- [ ] Real-time streaming transcription
- [ ] Clipboard content restoration after paste
- [ ] macOS support

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.
