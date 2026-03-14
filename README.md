# FAQ-ChatBot
This project is a **FAQ-based customer support chatbot** built using **Node.js** and the **OpenAI SDK (via OpenRouter)**. The chatbot answers user queries related to the QuickBite food delivery service by using a predefined FAQ dataset.

The bot is designed to respond **only with information provided in the FAQ** and avoids generating answers outside that dataset. If a user asks a question that is not covered in the FAQ or unrelated to QuickBite services, the chatbot politely declines and directs the user to contact support.

The project demonstrates how to build a controlled AI chatbot with guardrails to prevent hallucinations, off-topic responses, and unsafe interactions.

## How it Works

The chatbot sends a request to the AI model with a **system prompt** that includes the QuickBite FAQ data and rules. The model then generates a response based only on that information.

Key rules implemented in the system prompt:

* The chatbot answers **only using the provided FAQ data**
* If the question is not in the FAQ, it replies with
  *"I don't have information on that. Please contact [support@quickbite.com](mailto:support@quickbite.com)."*
* The bot maintains a **polite and empathetic tone**
* It does **not generate or invent policies or information**
* It avoids asking for **sensitive data** such as passwords, OTPs, or card numbers
* If a user sends abusive language, the bot asks them to **rephrase politely**

## Files in the Project

* `index.js` — Main chatbot program
* `faq.json` — Dataset containing QuickBite FAQ questions and answers
* `.env.example` — Example file showing required environment variables

This project shows how AI can be combined with a structured dataset to build a **reliable FAQ support chatbot**.
