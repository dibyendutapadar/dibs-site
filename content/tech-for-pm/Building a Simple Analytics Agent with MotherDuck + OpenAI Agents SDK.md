---
title: Building a Simple Analytics Agent with MotherDuck + OpenAI Agents SDK
date: 2025-12-01
summary: 
tags:
  - AI
  - openai
  - AIAgent
description:
keywords:
  - AI PM
  - Tech for PM
  - Product Manager Portfolio
  - open ai agents sdk
  - duckdb
  - motherduck
  - AI Agent
draft: false
categories:
  - AI PM
  - Tech for PM
  - AI Agents
slug: simple-analytics-agent-motherduck-openai-agents-sdk
weight: 5
cover:
  image: /img/motherduck_openai_agents.png
  alt: simple-analytics-agent-motherduck-openai-agents-sdk
---

_The quickest and cleanest possible way_

Many teams today want to let non-technical users query data using plain English instead of writing SQL or dashboards. I have been playing around with multiple frameworks and techniques to achieve this, and finally I landed upon open ai agenst sdk + motherduck data warehouse, this is the quickest, cleanest, effective and at the same time thoroughly customizable way I could find.

Combining MotherDuck’s data-warehousing power with agents that can generate and run SQL makes that possible. In this post I walk you through a minimal end-to-end example — how to wire up a simple agent that queries a database on MotherDuck.

## **Why use MotherDuck + OpenAI Agents SDK**

Before diving into code, a quick look at why this combo makes sense:

#### **MotherDuck’s strengths**

- MotherDuck gives you per-user (or per-tenant) isolation: each user (or customer) gets their own dedicated DuckDB instance (“duckling”), so analytics workloads don’t interfere with each other. That’s great for multi-tenant setups or customer-facing analytics.
- Because DuckDB is lightweight and embeddable, you get really low latency. You don’t need a heavyweight MPP cluster. That makes queries fast enough for interactive use.
- MotherDuck supports “AI + database” workflows: agents connected to MotherDuck can generate SQL, run queries, and fetch results — bridging LLMs and structured data elegantly.
- It’s free tier supports personal use, good for POC and experimentations

#### **OpenAI Agents SDK’s strengths**

- The SDK provides a minimal set of primitives (agents, tools, sessions, guardrails) that make it easy to build agentic apps.
- It lets you wrap any Python function as a “tool”: that means you can write a function to execute SQL (against MotherDuck), expose it as a tool, and let the agent call it dynamically.
- Because it’s Python-first and lightweight, you can prototype quickly without massive boilerplate.

Put together, this architecture lets you build natural-language analytics agents that query real data stored in a scalable, isolated, low-latency warehouse.

---

## High-level Flow

1. Get access (account + token) to MotherDuck and have a database loaded (or use the sample DB tables for experimentation like I will demonstrate in the sample code).
2. In Python, wrap a function that connects to MotherDuck (via DuckDB) and runs arbitrary SQL.
3. Use OpenAI Agents SDK to define an agent, expose your SQL runner as a tool.
4. Send natural language questions to the agent. The agent generates SQL, executes via the tool, returns results.

Below is the sample code illustrating this flow.

```python
# sample_agent.py  
  
from agents import Agent, Runner, function_tool  
import duckdb  
  
# Tool: runs SQL against MotherDuck  


@function_tool  
def run_sql(query: str) -> str:  
    """  
    Execute SQL query against MotherDuck and return results as string.  
    """  
    token = os.getenv("MOTHERDUCK_TOKEN")  
    conn = duckdb.connect(f"md:my_database?motherduck_token={token}", read_only=True)  
    try:  
        df = conn.execute(query).fetchdf()  
        return df.to_string(index=False)  
    except Exception as e:  
        return f"Error executing query: {e}"  
  
# Define the agent  
agent = Agent(  
    name="AnalyticsAgent",  
    instructions=(  
        "You are a data assistant. "  
        "When user asks a question about data, generate valid DuckDB SQL, "  
        "execute via run_sql tool, and return the result."  
    ),  
    tools=[run_sql],  
    # optionally configure model / temperature here  
)  
  
def ask(question: str):  
    result = Runner.run_sync(agent, question)  
    return result.final_output  
  
if __name__ == "__main__":  
    user_query = input("Ask something about data -> ")  
    print(ask(user_query))
```

- `run_sql`: a Python function decorated as a “tool” so the agent can call it whenever it needs to run SQL. It connects to your MotherDuck database (via DuckDB), executes the SQL, returns results.
- `Agent(...)`: creates an agent with a system prompt (instructions) telling it what its role is. We give it access to the `run_sql` tool.
- `Runner.run_sync(agent, ...)`: sends a user question, triggering the agent loop: the agent uses the LLM to generate SQL + reasoning, then calls `run_sql`, grabs results, returns them.

With this minimal setup, you already get a natural-language → structured-data interface.

For a full working code with a little enhancements such as adding a schema definition, query guidance which makes the agent response time shorter, crisper and cleaner, checkout the repo here:


[GitHub]](https://github.com/dibyendutapadar/simple-data-analytics-motherduck-openai-agents)