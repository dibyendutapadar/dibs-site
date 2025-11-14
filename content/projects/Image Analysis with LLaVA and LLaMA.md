---
title: Image Analysis with LLaVA and LLaMA
summary: Uses multimodal LLMs for domain-specific image understanding in marketing, education, and healthcare.
tags: ["LLaMA", "LLaVA", "CrewAI", "Streamlit", "AI Image Analysis"]
categories: ["Projects", "AI"]
draft: false
description: "Product Manager Portfolio showcasing my work"
keywords: ["AI PM", "Tech for PM", "Product Manager Portfolio", "PM Portfolio"]
weight: 3
cover:
  image: "/img/20251113212749.png"    
  alt: "Image Analysis"
---
# AI Agent to analyze your snaps.

How about a crew of AI agents who can sift through your snaps, pick the absolute best ones, and even whip up the perfect Instagram captions? Say goodbye to the endless selection and caption conundrums. With AI agents, we are stepping into the future of AI-powered creativity, where your snaps are transformed into Instagram hits without breaking a sweat.

## The "Insta Influencer" Image Analyzer

This nifty app is like having your very own Instagram manager on speed dial. Simply upload a bunch of images, and let the AI do the heavy lifting. It doesn’t just pick the best photo; it goes a step further by crafting a caption that’s not only on-trend but tailored to the vibe of your image. How? By harnessing the power of advanced AI models that understands images and what makes a post pop on Instagram.

  

🔗 Check out the Git repo here: [https://github.com/dibyendutapadar/ai-agent-image-analyzer](https://github.com/dibyendutapadar/ai-agent-image-analyzer)

## Demo: I provided the app some pics from Goa trip to analyze from.

_The response was quite astonishing form 8b models run on local. Notice how detailed the image descriptions are._

![Article content](https://media.licdn.com/dms/image/v2/D5612AQGbdZnhvb4Xnw/article-inline_image-shrink_1500_2232/article-inline_image-shrink_1500_2232/0/1723260869654?e=1764806400&v=beta&t=STD64pMtJNVUsGgmzybePbnaVcyWWY7ppT3OxxUPnLQ)

---

## The Tech That Makes It All Happen

### Large Language Models (LLMs)

At the heart of this magic is obviously LLMs (Large Language Models). LLMs have been game-changers in making our interactions with technology more natural, almost like chatting with a super-smart friend.

### LLaMA and LLAVA

Now, let’s talk about two key players: [**LLaMA**](https://llama.meta.com/) (Large Language Model Accelerated) and [LLAVA](https://www.microsoft.com/en-us/research/project/llava-large-language-and-vision-assistant/) (Large Language Vision Agent). LLaMA is one of your go-to LLM for processing text, while **LLaVA** is a novel end-to-end trained large multimodal model that combines a vision encoder and Vicuna for general-purpose visual and language understanding.

Together, they’re the dynamic duo that enables this app to seamlessly juggle both text and images.

_I have used 8b models of both, but if you have access to superior computing power (read GPU) you can use larger models as well_

### AI Agents and Crew AI

Here’s where it gets even cooler—AI agents. These are autonomous helpers that handle tasks for you. In our app, we use [CrewAI](https://www.crewai.com/) to coordinate these agents, making sure everything runs smoothly. It’s like having a team of experts working behind the scenes to ensure your photos and captions are on point.

## How It All Comes Together

So, how exactly we select from photos into Instagram-worthy posts? Let’s break it down:

1. **Upload Your Photos**: Start by uploading your images—whether they’re in PNG, JPG, or JPEG format.
2. **AI Image Analysis**: The magic begins as LLAVA gets to work, analyzing your images to extract detailed descriptions. It’s like having an art critic and a storyteller rolled into one, interpreting each photo.
3. **Crafting the Perfect Caption**: Armed with these descriptions the agent then picks the best image and writes a caption that’s primed for maximum engagement. It considers everything from trending hashtags to current events.
4. **AI Agent in Action**: Crew AI coordinates the process, ensuring that the agent’s decisions are spot on. The agent doesn’t just pick a photo and write a caption; it does so with a clear strategy in mind, maximizing your post’s potential to go viral.
5. **Your Ready-Made Instagram Post**: Finally, the app presents the results in a clean, easy-to-use format. You get a detailed breakdown of all your photos, the chosen winner with an explanation, and a caption ready to be copied and pasted straight into Instagram.

And the best part about this,

> All this is achieved without any need to train the model on own data.

Gone are the days of scrambling to gather massive datasets just to get started. These pre-trained models give you a serious head start. Sure, you can fine-tune them with your specific data to make them even better, but as you can see from the results, they’re already delivering impressive outcomes right out of the box.

## What's the big deal? ChatGPT can already do this.

Of course, it can—but there’s a catch. While GPT-4 and its image processing capabilities can handle similar tasks, these features often come with a _price tag_.

Plus, our app is a playground for these ideas, offering a fun, user-friendly way to explore what AI can do with your images. Now, imagine scaling this up for industrial use cases. Organizations can employ similar methodologies to **tackle specific challenges unique to their operations—without the worry of sharing sensitive information with a third-party service like ChatGPT**.

**In-house AI solutions** provide a tailored approach, ensuring privacy and control over proprietary data.

## Beyond a toy app to Organizational use cases

Below are some industry use cases where images are too sensitive and confidential to be exposed to third part service provider. Getting LLMs deployed on premise, can help maintian the secrecy and getting the job done.

### HealthTech

- **Medical Imaging**: Assist in diagnosing conditions from X-rays to MRIs.

_Lets see this in action. It was fascinating to see how much can be achieved without any fine tuning from a 8b vision model and a 8b text model with 30 lines of code on a personal laptop_

![Article content](https://media.licdn.com/dms/image/v2/D5612AQEmSZQco6m5cA/article-inline_image-shrink_1000_1488/article-inline_image-shrink_1000_1488/0/1723255477584?e=1764806400&v=beta&t=b1QqEEj990LA-f-TiqVVF_CoIs_cbplfAO3UwmWs18I)

### EdTech

- **Grading Exams**: Automate grading for handwritten exams, ensuring fairness and speed. (I have a hunch that with the democratisation of GenAI, handwritten exams are going to come back. For EdTech enthusiasts, you can read this study on the effect of GenAI on education)

![Article content](https://media.licdn.com/dms/image/v2/D5612AQEonkG10lr9Xw/article-inline_image-shrink_1500_2232/article-inline_image-shrink_1500_2232/0/1723259018627?e=1764806400&v=beta&t=aZA8IFe6YVuOemG2x_dm_BCcNWoIacPGjt8qp5_XIEA)

_Let's see how an untuned model can provide a head start for evaluation of answer scripts._

![Article content](https://media.licdn.com/dms/image/v2/D5612AQE1zdlB80DJBQ/article-inline_image-shrink_1500_2232/article-inline_image-shrink_1500_2232/0/1723259814959?e=1764806400&v=beta&t=RXENn2lXhT-YKJbeZ2xvkf5NqTAfjTxRR9RLxPbUI1A)

  

  

It can also be used in other sectors where information is absolutely confidential

### FinTech

- **Customer Verification**: Automate document verification with image analysis.

### Insurance

- **Claims Processing**: Quickly assess damages with image evaluation.

---

**Technologies Used**: LLaMA, LLaVA, CrewAI, Streamlit  

🔗 [GitHub](#)  

📝 [Read on LinkedIn](https://www.linkedin.com/pulse/ai-agent-analyze-your-snaps-dibyendu-tapadar-ib3uc)
