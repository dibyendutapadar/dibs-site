---
title: How I Built a Writing Agent using Google ADK to Match My Writing Style
date: 2025-12-07
summary: Mult Agent Orchestrated Blog writer using Google ADK, that learns and matches users writing style
tags:
  - AI
  - google-adk
  - multi-agent
description:
keywords:
  - AI PM
  - Tech for PM
  - Product Manager Portfolio
  - Google ADK
  - Multi Agent Orchestration
  - Agentic AI
draft: false
categories:
  - AI Agents
slug: how-i-built-a-writing-agent-using-google-adk-to-match-my-writing-style
weight: 1
cover:
  image: /img/blog-writer.png
  alt: alt
---

For a while now, my LinkedIn feed has been a canvas for my thoughts and insights, a place where I’ve honed my perspectives and showcased my experiments.

To make things a little structured I though of launching my own portfolio and blog website to house these writings, expand on new topics by categories and connect more deeply with my audience. I built this website with a very effective  [Obsidian](https://obsidian.md) — [Hugo Papermod](https://themes.gohugo.io/themes/hugo-papermod/)-  [Netlify](https://netlify.com)  combo, and hosted via Cloudfare.

Now, writing  _a lot_  is a lot of work, and that too constant writing. I initially turned to tools like ChatGPT to help generate initial drafts, hoping to speed up the process. While powerful, I quickly ran into a few persistent frustrations.

-   The back-and-forth required to get a decent draft was excessive
-   Context was often forgotten in longer conversations, and most importantly,

> **It consistently failed to capture  _my_  distinctive writing style — the tone, the rhythm, the specific way I phrase things.**

It felt like I was spending more time editing to make it sound like me than I would have writing from scratch.

That’s when I decided to take matters into my own hands. I needed a solution that understood my style, remembered our interactions, and could quickly produce initial drafts that genuinely sounded like  _me_. I was exploring agentic frameworks and thought, why not build an agent that solves my oen pain point first.

### Introducing My Custom Article Writing Agent ADK

This project, an article writing agent built using the Google ADK (Agent Development Kit) framework, is my solution to those content creation woes. It’s designed to automate the initial drafting process, allowing me to focus on refining, adding depth, and bringing my unique perspective to the forefront, rather than wrestling with generic AI output.

  

### How It Works: A Collaborative Team of Agents

Here’s a look at the workflow:

1.  **General Web Search Agent**: Every great article starts with solid research. This agent kicks things off by performing in-depth web searches on a given topic and synthesizing key findings. It uses the  `google_search`  tool to gather the latest information, ensuring the content is well-informed and up-to-date.
2.  **Aggregator Agent**: Once the research is complete, the Aggregator Agent steps in. Its job is to take all the raw findings from the General Web Search Agent and synthesize them into a coherent, well-structured research brief. This brief then serves as the foundation for the drafting process.
3.  **The Drafting Loop (The Heart of the System)**: This is where the magic of style matching truly happens, in an iterative cycle designed for continuous improvement:
	1. **Writer Agent**: Using the aggregated research brief, this agent creates the initial draft of the article. It focuses on clarity, structure, and engaging content.
	2. **Style Review Agent**: This is the secret sauce for personalization. Before it even looks at the draft, this agent calls a special tool (`get_writing_style`) that fetches my personal writing samples from a  `writing_style.md`  file. It then meticulously analyzes my tone, language, and overall "throw" to understand my unique voice. With that understanding, it suggests specific rewrites to the draft to align it perfectly with my established style. I’ve leveraged a more powerful model like  `gemini-2.5-pro`  here to ensure nuanced style analysis.
	3. **Revision Agent**: Acting as the lead editor, this agent takes input from both the initial writer and the style reviewer. It ensures the article is complete, incorporates all the user’s original pointers, and crucially, makes sure it matches my style. It’s designed to refine and summarize changes, pushing the article back into the loop for further iterations if needed (currently set for up to 2 cycles) until it’s polished.
4. **Formatter Agent**: Finally, once the article has been through the drafting and revision loops and is fully approved, the Formatter Agent takes over. It transforms the content into clean, readable markdown, complete with appropriate headings, lists, bolding, italics, and blockquotes, ready for immediate publication.

  

---

Here’s how you can get started with the Google ADK framework:
Copy the repo from here : [Github](https://github.com/dibyendutapadar/article_writing_agent_adk)

1.  **Install Google ADK**: It’s as simple as  `pip install google-adk`.
2.  **Create an Agent**: Use  `adk create <folder_name>`  to set up your project structure.
3.  **Update Your** `**.env**` **File**: Securely include your API key for authentication.
4.  **Provide Your Writing Style Sample**: This is  _critical_  for style matching. Create a  `writing_style.md`  file and fill it with samples of your writing. The more content you provide, the better the Style Review Agent can learn and replicate your unique voice.
5.  **Refine Prompts**: Tweak the prompts in the  `agent.py`  file to perfectly align with your specific needs and preferences.
6.  **Run the Agent**: Start your agent locally with  `adk run web`  and prompt it to bring your content ideas to well framed drafts in your own style.