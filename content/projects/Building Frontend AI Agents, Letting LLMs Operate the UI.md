---
title: Building Frontend AI Agents, Letting LLMs Operate the UI
summary: Enables AI agents to perform automation and take action on frontends, via playwright mcp
tags:
  - GenAI
  - AIAgent
  - google-adk
  - automation
categories:
  - Projects
  - AI
description: Product Manager Portfolio showcasing my work
keywords:
  - AI PM
  - Tech for PM
  - Product Manager Portfolio
  - PM Portfolio
  - AI in Enterprise
  - Generative AI Use Cases
draft: false
weight: 1
cover:
  image: /img/frontend-automation.png
  alt: Chat with Local Documents
---
## The Shift from Text to Action

  

Can AI agents take actions on frontends on behalf of users?

Most AI agents today stop at text generation. They can write code, summarize emails, or chat about your data, but they struggle to *cross the chasm* into the physical (or digital) world of user interfaces. A major shift is happening: AI agents are evolving to operate interfaces that were never designed for machines, completing complex workflows just as a human would.

  

In this project, I explored the architecture of a **Frontend AI Agent**. By combining the **Google ADK (Agent Development Kit)** framework with the **Playwright Model Context Protocol (MCP)**, I’ve built a system where an LLM understands user intent and directly operates the UI—navigating pages, reading DOM elements, clicking buttons, and filling forms without a single line of brittle, hardcoded selectors.

  

---

  

## Why Frontend Automation Needs AI

  

Traditional frontend automation (like Selenium or standard Playwright scripts) is notoriously "flaky." It relies on hardcoded CSS selectors or XPath expressions. The moment a developer changes a class name or moves a button, the script breaks.

  

**Intent-Driven Automation** changes the game. Instead of telling the computer *how* to do it (e.g., "Click the button with id 'submit-01'"), we tell the agent *what* we want (e.g., "Submit the registration form with my profile details").

  

The agent uses its reasoning capabilities to:

1.  **Perceive**: Inspect the page structure and visual state.

2.  **Reason**: Determine which elements are relevant to the user’s goal.

3.  **Act**: Execute precise interactions (clicks, typing, etc.) via the browser.

  

---

  

## The Tech Stack: Wiring the Brain to the Hands

  

This experiment leverages three core technologies to create a seamless automation loop:

  

### 1. Google ADK (The Brain)

The [Google Agent Development Kit](https://google.github.io/adk-docs/) acts as the orchestrator. It manages the agent's memory, tools, and the interaction cycle. It provides a robust framework for defining "Instruction Sets"—the operating policies that guide how the agent behaves.

  

### 2. Playwright MCP (The Hands)

[Playwright MCP](https://github.com/microsoft/playwright-mcp) is a standardized tool interface based on the Model Context Protocol. It exposes browser capabilities (navigation, clicks, screenshots) as "tools" that the LLM can call. This abstraction allows the LLM to interact with a real Chrome/Chromium instance through a clean, programmatic interface.

  

### 3. LLMs (The Reasoning Engine)

I used `gpt-4o` and `gemini-1.5-pro` as the logic layer. These models are capable of understanding complex layouts and mapping high-level user requests to low-level browser actions.


---

  

## Use Cases: From Testing to Live Action

  

This pattern extends far beyond simple scripts. Two specific use cases stand out:

  

### 1. Intent-Driven Frontend Testing

Imagine a world where QA engineers don't write scripts. They write "Intents."

*  *"Verify that a user from Germany can add a product to the cart and see the correct VAT in the checkout."*

The agent figures out the path, handles the UI variations, and reports back. This makes testing resilient to UI changes and significantly faster to implement.

  

### 2. In-Situ AI Agents in Complex SaaS (ERPs)

Enterprises are filled with complex systems like SAP, Oracle, or custom ERPs that are difficult to navigate. A frontend AI agent can act as an "overlay," helping users complete tasks.

*  *User: "Adjust the Q3 forecast for the North America region by 10%."*

The agent navigates the complex screens, performs the multi-step action, and asks for confirmation only when necessary. It’s not just a "help chatbot"—it’s a **Live Workflow Completer**.

  

---

  

## The Gap Between Knowing and Doing

  

Most "Co-pilots" today are passive; they wait for you to ask and then they answer. The next generation of SaaS will be **Agentic**.

  

By integrating tools like **Playwright MCP** and **Google ADK**, we are closing the gap between *knowing* what needs to be done and *doing* it. We are moving from a world where we operate software to a world where we collaborate with agents that operate software on our behalf.