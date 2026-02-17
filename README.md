# Kaagapay — Ang Imo Abyan

Kaagapay is a free, private, locally-run AI wellness companion that speaks Hiligaynon. It is designed to feel like chatting with a caring friend — warm, non-judgmental, and always ready to listen. Built on top of [Ollama](https://ollama.com) and the `llama3.2` language model.

> *"Kaagapay" means companion or helper in Hiligaynon.*

---

## Live Demo

https://lordbeejay.github.io/Kaagapay/

Note: The website is just the chat interface. The AI runs on your own computer, so you need to complete the setup below before using it.

---

## How It Works

Kaagapay runs entirely on your local machine. When you send a message, the website talks to Ollama running in the background on your computer. No data is sent to any external server — your conversations stay completely private.

---

## Requirements

- Windows, macOS, or Linux
- At least 8GB of RAM (16GB recommended)
- About 3–5GB of free disk space
- [Ollama](https://ollama.com/download) installed

---

## Setup Instructions

**Step 1 — Install Ollama**

Download and install Ollama from [https://ollama.com/download](https://ollama.com/download).

**Step 2 — Download the base model**

Open your terminal or command prompt and run:

```
ollama pull llama3.2
```

**Step 3 — Download the Modelfile**

Download the `Modelfile` from this repository and save it to a folder on your computer.

**Step 4 — Build the Kaagapay model**

In your terminal, navigate to the folder where you saved the Modelfile and run:

```
ollama create kaagapay -f Modelfile
```

**Step 5 — Start Ollama with CORS enabled**

This allows the website to connect to Ollama on your computer.

macOS / Linux:
```
OLLAMA_ORIGINS=* ollama serve
```

Windows (Command Prompt):
```
set OLLAMA_ORIGINS=* && ollama serve
```

Windows (PowerShell):
```
$env:OLLAMA_ORIGINS="*"; ollama serve
```

**Step 6 — Open the website**

Go to [https://YOUR-USERNAME.github.io/kaagapay/](https://YOUR-USERNAME.github.io/kaagapay/) and start chatting.

---

## Features

- Speaks natural, everyday Hiligaynon with some Tagalog and English mixed in
- Warm and grounded tone — like talking to a trusted friend, not a robot
- Guided by real counseling principles: empathic listening, person-centered therapy, and CBT techniques
- Crisis-aware — gently encourages professional help when needed
- Fully private — nothing leaves your computer
- No account, no subscription, no internet required after setup

---

## Troubleshooting

**"Cannot connect to Kaagapay" error**
Make sure Ollama is running with `OLLAMA_ORIGINS=*`. Close and reopen the terminal and try again.

**Ollama is not recognized as a command**
Restart your computer after installing Ollama, then try again.

**Kaagapay responds in English instead of Hiligaynon**
Rebuild the model: `ollama create kaagapay -f Modelfile`. Make sure the Modelfile was not renamed to `Modelfile.txt`.

**The website loads but responses are very slow**
This is normal on lower-end hardware. Close other applications to free up RAM.

---

## Privacy

All conversations happen locally on your device. The website does not collect, transmit, or store any data. Ollama itself does not send your conversations anywhere.

---

## Disclaimer

Kaagapay is a supportive companion tool, not a licensed mental health professional. It is not a substitute for therapy or professional counseling. If you or someone you know is in crisis, please contact a professional.

Philippines Crisis Hotline: 1553 (Hopeline, free, 24/7)

---

## Built With

- [Ollama](https://ollama.com) — local LLM runtime
- [llama3.2](https://ollama.com/library/llama3.2) — base language model
- Vanilla HTML, CSS, and JavaScript — no frameworks or dependencies
