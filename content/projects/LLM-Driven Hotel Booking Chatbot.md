---
title: LLM-Driven Hotel Booking Chatbot
summary: Real-time conversational booking assistant powered by Groq API and Streamlit.
tags:
  - LLM
  - Chatbot
  - Streamlit
  - Groq
  - GenAI
categories:
  - Projects
  - AI
draft: false
description: Product Manager Portfolio showcasing my work
keywords:
  - AI PM
  - Tech for PM
  - Product Manager Portfolio
  - PM Portfolio
  - AI in Travel
  - GenAI in Travel
  - Generative AI Use Cases
weight: 6
cover:
  image: /img/20251113212301.png
  alt: LLM-Driven Hotel Booking Chatbot
---
# An Experiment to disguise Open Source LLM as a Hotel Bookings Agent!!

### TL;DR

Harnessing the power of open-source LLMs like Llama 3.1, I've tried to create a chatbot that simplifies hotel bookings, using "**llama-3.1-8b-instant"** model, **Groq** for enhanced AI performance and **Streamlit** for a seamless web interface. The chatbot can answer user queries, remember chat contexts, take and manage bookings.

🎥 [Watch the demo video](https://youtu.be/wjZpTwGxS-w)

🔗 [Check out the application on Streamlit Cloud](https://hotel-chatbot.streamlit.app/)

  

### Background

In the ever-evolving world of artificial intelligence, the advent of open-source Large Language Models (LLMs) like DCLM and Llama 3.1 has been looked at as a game-changer. But without real-world application, a good technology is like a work of art, valuable but not tangible.

For the past few days, I've been contemplating how we can harness these powerful tools. Coincidentally, while planning a weekend getaway, I found myself booking a hotel room through a WhatsApp conversation with a human receptionist. This got me thinking: can we use an LLM to handle bookings just as effectively? It seemed like a long shot, but I decided to give it a try.


### Discovering the Tools: Groq and Streamlit

During my research, I came across Groq and Streamlit:

- **Groq**: Imagine a super-efficient engine designed to accelerate machine learning models. Groq's hardware and software solutions enhance the performance of AI applications, making them faster and more reliable. [[https://groq.com/](https://groq.com/)]
- **Streamlit**: Think of Streamlit as a magic wand that turns your data scripts into shareable web apps. It's a framework that allows you to create interactive websites from simple Python scripts, making data insights accessible and engaging. And streamlit-cloud makes the hosting a breeze. [[https://streamlit.io/](https://streamlit.io/)]

  

### Building the Chatbot

With these tools in hand and a little help from ChatGPT, I embarked on creating a chatbot to assist users with hotel bookings.

**The Flow of the Code:**

1. **Hotel Information in JSON**: The hotel details, including room types, prices, availability, and amenities, are structured in a JSON format. This ensures that the data is easily accessible and manageable.
2. **Passing Context to the LLM**: This JSON data is passed as context to the LLM model ("llama-3.1-8b-instant") via the Groq API, enabling the chatbot to respond with accurate and relevant information.
3. **Maintaining Chat Sessions**: Consecutive chats in the session are also passed to the Groq API, ensuring that the bot remembers the flow of the conversation and maintains context throughout the interaction.
4. **Streamlit as the FrontEnd:** used streamlit to provide a forntend to the interaction happening in the chat

👉 [Check out the code in GitHub](https://github.com/dibyendutapadar/streamlit_groq_chatbot)

### Where can it lead to?

1. **Dynamic Data Integration**: While I used static information, the system can easily be adapted to pull live data from various sources, keeping the chatbot updated with current prices and availability.
2. **WhatsApp, Call? why not**: Although I hosted the application on Streamlit, we can scale it, manage webhooks with [**ngrok**](https://ngrok.com/)**,** integrate it with platforms like [**Twilio**](https://www.twilio.com/en-us) to manage WhatsApp/SMS/Call interactions, or use text-to-speech AIs like [vapi.ai](http://vapi.ai/) for real-time conversations.
3. **Automated Booking Management**: The chatbot can update booking information in a database, send confirmation emails to users, and remember past contexts from sessions to handle any follow-up queries seamlessly.

  

### Potential Use Cases:

The applications of this technology extend far beyond the hospitality industry. Here are a few exciting possibilities:

- **Healthcare**: Streamlining patient appointments and managing inquiries.
- **Retail**: Assisting customers with product searches and order placements.
- **Finance**: Providing customer support for banking services and loan applications.
- **Education**: Facilitating enrollment processes and answering student queries.

  

### The Advantages of LLM based chat bots:

- The chatbot will respond naturally, so users won't feel like they're talking to a bot or navigating an IVR system. The user won't be prompted to select one from the below options. The LLM can adapt to the conversation and provide personalized responses each time, enhancing the user experience.
- We don't need to have huge set of data/ sample interactions to train the chatbots. Though they certainly be beneficial, but we can start fast, reducing the time to market. The bot can be provided with basic context and data, and it would perform quite well. This wouldn't have been possible without this open sourced LLMs.

---

**Technologies Used**: LLM, Groq API, Streamlit  

🔗 [GitHub](https://github.com/dibyendutapadar/streamlit_groq_chatbot)  

📝 [Article](https://www.linkedin.com/pulse/experiment-disguise-open-source-llm-hotel-bookings-agent-tapadar-osnfc)  

📱 [App Link](https://hotel-chatbot.streamlit.app/)
