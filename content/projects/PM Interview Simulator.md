---
title: Interview Simulator
summary: Custom GPT model simulating realistic product management interviews.
tags: ["GPT", "Interview Simulation", "Prompt Engineering"]
categories: ["Projects", "AI"]
draft: false
weight: 9
cover:
  image: "/img/20251109185651.png"    
  alt: "Cover image alt text"
---

In case you want to skip everything and try the simulator:

[PM interview simulator](https://chatgpt.com/g/g-9sJq1K1kg-product-management-interview-simulator)

Practice makes perfect, and nowhere is this truer than in the realm of interviews. The more you practice, read, and learn, the more adept you become. For those preparing for product management interviews at junior and assistant levels, two books often come highly recommended: **Cracking the PM Interview** and **Decode and Conquer**. These books are celebrated for their conversational examples between interviewers and candidates, which help readers grasp the interview dynamics effectively. With the advent of powerful tools like ChatGPT, one would expect interview preparation to be easier. 

**Why did I create this?** 

While preparing for PM interviews, we noticed that the responses from general GPTs often lacked the realistic flow and format expected by interviewers. So, we decided to create a solution that bridges this gap, helping you practice effectively and confidently.

  

### Let's try out the most popular vanilla GPTs with a generic design question 

> **Design an alarm clock for the blind**

###### Here is the response from **ChatGPT-4o.**

![ree](https://static.wixstatic.com/media/f3d706_2b89e072aa98457c9548b3984dbc8416~mv2.png/v1/fill/w_966,h_1000,al_c,q_90,enc_avif,quality_auto/f3d706_2b89e072aa98457c9548b3984dbc8416~mv2.png)

  

  

###### And here’s the same question posted to Claude: 

![ree](https://static.wixstatic.com/media/f3d706_05feb095f5f64090a7a2f2ddbbd752ea~mv2.png/v1/fill/w_1480,h_824,al_c,q_90,usm_0.66_1.00_0.01,enc_avif,quality_auto/f3d706_05feb095f5f64090a7a2f2ddbbd752ea~mv2.png)

  

  

Let's try one more, this time an RCA question

> Ola is experiencing a 25% decrease in daily ride bookings. How would you identify the root cause of this decline and propose solutions?

###### Let's see how chatgpt performs

![ree](https://static.wixstatic.com/media/f3d706_0a41d05b24c44ae888166f8f8a5614c5~mv2.png/v1/fill/w_924,h_1000,al_c,q_90,enc_avif,quality_auto/f3d706_0a41d05b24c44ae888166f8f8a5614c5~mv2.png)

  

  

###### And here's how Claude performs

  

![ree](https://static.wixstatic.com/media/f3d706_e83128155ed344ba91889530f6977630~mv2.png/v1/fill/w_1252,h_1000,al_c,q_90,enc_avif,quality_auto/f3d706_e83128155ed344ba91889530f6977630~mv2.png)

  

Though these are valuable insights, but not exactly how the interviewer expects the answer structure. Let's try to **prompt to act as a PM interview candidate** and answer the question.

![ree](https://static.wixstatic.com/media/f3d706_fe41aadd9065431a8970b6b30bb46a5d~mv2.png/v1/fill/w_970,h_1000,al_c,q_90,enc_avif,quality_auto/f3d706_fe41aadd9065431a8970b6b30bb46a5d~mv2.png)

  

  

It’s clear that the responses are quite generic, lacking the structured and realistic flow expected in an actual interview.

  

## Bridging the Gap: Introducing the ‘Product Management Interview Simulator’

To address this gap, I created a custom GPT tailored specifically to help PM aspirants prepare for interviews. I’ve named it the **‘Product Management Interview Simulator’**. 

  

  

## Let’s see how the custom GPT handles the same questions: 

**What to expect?**

**Detailed and Structured Responses:** Get answers that follow the proper format, including clarifying questions and realistic scenarios enacting the interviewer and the interviewee.

### The Design Question

  

![ree](https://static.wixstatic.com/media/f3d706_db576b22bec84e2e9184e7f866024592~mv2.png/v1/fill/w_956,h_1000,al_c,q_90,enc_avif,quality_auto/f3d706_db576b22bec84e2e9184e7f866024592~mv2.png)

  

If you have ever prepared for PM interviews, this response looks much more realistic and acceptable right?

### The RCA Question

![ree](https://static.wixstatic.com/media/f3d706_5bafb51265864ba6897cab060b6275c9~mv2.png/v1/fill/w_1069,h_1000,al_c,q_90,enc_avif,quality_auto/f3d706_5bafb51265864ba6897cab060b6275c9~mv2.png)

  

  

As you can see, this simulator closely mimics real-world scenarios, asking clarifying questions and following a proper flow and format.

### How Did I Train the GPT?

Creating this custom GPT involved leveraging ChatGPT’s capabilities for training with prompts and custom data. For the training data, I scraped a wealth of mock interviews from various sources:

  

- PDFs of relevant books
    
- Transcripts of YouTube videos
    
- Posts from product management communities
    
- Blogs dedicated to PM topics
    

  

I then cleaned and structured this data into a JSON format, a snippet as below:

The JSON file includes the question, related product, product type, question keyword, question type, and a detailed interaction between the interviewer and interviewee.

### Focus Areas

I initially focused on five key question types, which are commonly asked for in PM interviews

  

1. **Product Design**
    
2. **Root Cause Analysis (RCA)**
    
3. **Problem Solving**
    
4. **Product Improvement**
    
5. **Product Metrics**
    

  

By providing detailed context and employing few-shot prompting techniques, I configured the GPT to understand and format responses appropriately for the approach to different types of questions.

  

### Your Feedback Matters to Me

While the GPT is still a work in progress, I am eager for feedback from the Product Management Community. 

If you’re interested, please visit the custom GPT, try it out with different types of questions [out of the question-types mentioned above], and share your thoughts.

Here is the link to the custom GPT:

[PM Interview Simulator](https://chatgpt.com/g/g-9sJq1K1kg-product-management-interview-simulator)

Your input will not only help improve the tool but also help to reach fellow PM aspirants in their journey towards acing their interviews. Happy practicing!

  

### Feedback

Your feedback (whether in my inbox, comments, or through a rating) will be immensely valuable.

You can click on the down arrow beside the GPT name on top left, and click on **'Review GPT'** to post a rating 

Though you need to be a premium member to rate, however you just need to login to ChatGPT to use the simulator.

  

  

## Disclaimer

These are LLMs and they can make mistake. They are not a replacement of creative, cognitive. logical and strategic thinking. The responses should only be taken as food for thought while practicing and exploring different types of questions.