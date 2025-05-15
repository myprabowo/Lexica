# 🤖 Lexica — Learning English eXperiences via Intelligent Conversational Agent

Lexica is an intelligent conversational agent for learning English, powered by **n8n**, **Google Gemini AI**, and **Telegram Bot API**. It delivers **adaptive, CEFR-aligned learning experiences** by engaging users through interactive conversations.

---

## 🌟 Features

- ✅ **Telegram integration** to receive and respond to text, voice, and image messages.
- 🧠 **AI-powered English learning assistant** with a supportive, level-aware teaching style.
- 🌐 **CEFR-based personalization** (A1–C2), dynamically adapting tasks to user proficiency.
- 📸 **Image understanding**: Users can send pictures to receive English descriptions.
- 🗣️ **Multimodal input support**: Works with text, images, and audio.
- 🇬🇧🇮🇩 **Bilingual guidance**: English learning instructions with optional Indonesian clarification for beginners.

---

## 📦 Project Structure

This repository contains:

- `lexica-n8n-workflow.json`: The exported n8n workflow containing all automation nodes.

The workflow includes:

| Node Name              | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Telegram Trigger        | Listens for incoming Telegram messages (text, photo, audio).               |
| Switch                  | Routes input based on content type (Text, Image, Audio).                   |
| AI Agent (Langchain)    | Handles text-based conversation using CEFR-aligned logic and personality.  |
| Google Gemini Chat Model| Processes AI responses via Gemini 2.0 Flash model.                         |
| Check Prompt            | Extracts image caption or assigns default prompt.                          |
| Call Gemini API         | Sends image and prompt to Gemini for description.                          |
| Merge                   | Combines image data and user prompt.                                       |
| Telegram (Send Output)  | Sends AI-generated reply back to the user.                                 |

---

## 🚀 Getting Started

1. **Clone this repository** and import the JSON file into your **n8n** instance.
2. Set up the following credentials in your n8n environment:
   - Telegram Bot API (`telegramApi`)
   - Google Gemini / PaLM API (`googlePalmApi`)
3. Deploy the workflow and connect your Telegram bot.
4. Chat with Lexica by sending:
   - Text messages to receive CEFR-based learning tasks.
   - Images for English descriptions.
   - Voice notes.

---

## 🎓 CEFR Level Adaptation

Lexica tailors its prompts and feedback to the user’s CEFR level:

| Level | Focus Area                              | Example Prompt |
|-------|------------------------------------------|----------------|
| A1    | Basic words & simple sentences          | *“What’s your favorite color?”* |
| A2    | Simple past & expressions               | *“Tell me what you did last weekend.”* |
| B1    | Storytelling & opinion sharing          | *“Describe a fun day using ‘first, then, finally.’”* |
| B2    | Argumentation & abstract thinking       | *“Do you agree with online learning? Why?”* |
| C1    | Critical thinking & idiomatic use       | *“What’s the difference between ‘hope’ and ‘wish’?”* |
| C2    | Formal, academic, and stylistic variation| *“Write a short essay on AI in language learning.”* |

---

## 🤝 Contribution

Have ideas to enhance Lexica (e.g., audio feedback, session memory, gamification)? Feel free to fork and suggest improvements.

---

## 📜 License

This project is under the [MIT License](LICENSE).

---

## 🧠 About

Lexica was built as part of an AI hackathon initiative to explore how intelligent agents can support personalized English learning in a scalable, engaging, and context-aware way — all within an open automation platform like **n8n**.

---

> **“Learning a language is a journey — Lexica is here to walk it with you.”** 🌍
