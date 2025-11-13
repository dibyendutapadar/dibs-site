---
title: Adaptive Learning without Question-Answer Dataset
summary: Generates adaptive learning assessments dynamically using GenAI and proficiency tracking.
tags: ["Adaptive Learning", "GenAI", "LlamaIndex", "EdTech"]
categories: ["Projects", "AI", "EdTech"]
draft: false
weight: 4
cover:
  image: "/img/20251113213630.png"    
  alt: "Adaptive Learning without Question-Answer Dataset"
---


# 🌟 𝗖𝗮𝗻 𝘄𝗲 𝗰𝗿𝗲𝗮𝘁𝗲 𝗮𝗻 𝗮𝗱𝗮𝗽𝘁𝗶𝘃𝗲 𝗟𝗲𝗮𝗿𝗻𝗶𝗻𝗴 𝗔𝗽𝗽 𝘂𝘀𝗶𝗻𝗴 𝗟𝗟𝗠 𝘄𝗶𝘁𝗵𝗼𝘂𝘁 𝗮 𝗾𝘂𝗲𝘀𝘁𝗶𝗼𝗻 𝗮𝗻𝘀𝘄𝗲𝗿 𝗱𝗮𝘁𝗮𝘀𝗲𝘁? 🤔  
  
I gave it a try! 🚀  
  
 I built an app on [Streamlit](https://www.linkedin.com/company/streamlit/) utilizing [LlamaIndex](https://www.linkedin.com/company/llamaindex/). It takes in key information fromt he user , wraps it in a prompt, and uses [Groq](https://www.linkedin.com/company/groq/) inference API for a small **𝗟𝗟𝗠 (𝗹𝗹𝗮𝗺𝗮𝟯.𝟭-𝟴𝗯-𝗶𝗻𝘀𝘁𝗮𝗻𝘁)** to generate responses. By leveraging **𝗽𝘆𝗱𝗮𝗻𝘁𝗶𝗰**, we generate structured output in format that can be made as a multiple choice question, and the in-between data storage plus proficiency calculations are handled by **𝗦𝗤𝗟𝗶𝘁𝗲**. Based on the calculation, after each answer, the LLM is prompted with the difficulty level of the next question to be generated.  
  
🔗 You can try out the app here: [https://lnkd.in/gtXUHWMp](https://lnkd.in/gtXUHWMp)  
  
### 💡 𝗙𝗶𝗻𝗱𝗶𝗻𝗴𝘀:  
The answer is both yes and no! We can jumpstart by using the data the LLM was trained on. Even a small model does a fair job, but limited and un-curated knowledge base hampers the experience.  
However, this can be tackled with **𝗥𝗔𝗚 𝘁𝗲𝗰𝗵𝗻𝗶𝗾𝘂𝗲𝘀**. Where the exact contextual data can be retrieved from documents (books, PDFs, databases, PPTs, Videos) and then augmented by using an LLM. Particularly Graph RAG is showing promising potential for these kind of knowledge driven problem  
  
### 🤔 𝗣𝗼𝘀𝘀𝗶𝗯𝗶𝗹𝗶𝘁𝗶𝗲𝘀:  
  
🎯 **𝗔𝗱𝗮𝗽𝘁𝗶𝘃𝗲 𝗟𝗲𝗮𝗿𝗻𝗶𝗻𝗴:** Generates questions matching a learner's proficiency. Using knowledge graph the system can even be made to understand pre-grade learning gaps of the learner.  
📚 **𝗗𝘆𝗻𝗮𝗺𝗶𝗰 𝗖𝗼𝗻𝘁𝗲𝗻𝘁:** Creates content tailored to individual learning gaps (text, image, audio, video via multimodal LLMs). Should be an improvement over the long MOOCs, which starts and ends at the same level and follows the same path for every learner.  
🧠 **𝗖𝗼𝗻𝘁𝗲𝘅𝘁𝘂𝗮𝗹 𝗟𝗲𝗮𝗿𝗻𝗶𝗻𝗴:** Customizes content to the learner's interests, like teaching math to a cricket enthusiast student using cricket examples. And the best part, we don't need to have curated datasets to do that, it can be generated. 🏏⚾  
  
AI's (Specifically GenAI's) impact on education is being debated heavily, and rightly so. But can we ignore its potential? I don’t think we can! 🤖✨

**Technologies Used**: Python, Groq, LlamaIndex, Llama 3.1-8B, SQLite, Streamlit, Pydantic  

---

🔗 [GitHub](https://github.com/dibyendutapadar/adaptive-learning)  
📝 [Read on ](https://www.linkedin.com/posts/dibyendu-tapadar_ai-edtech-genai-activity-7232618708748095489-7lRV/)  
📱 [App Link](https://adaptive-learning.streamlit.app/)

---
