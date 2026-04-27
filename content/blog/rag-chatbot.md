---
title: "Building a RAG Chatbot for My Portfolio"
date: 2026-04-27
draft: false
description: "Creating an AI chatbot that understands my portfolio content using Retrieval-Augmented Generation (RAG)."
tags: ["AI", "RAG", "Chatbot", "Dify", "Portfolio"]
---

# Building a RAG Chatbot for My Portfolio

As part of my work with AI-driven applications, I wanted to explore how modern language models can be integrated into real software in a practical way. My goal was to build a chatbot for my portfolio website that could answer questions about me, my projects, and the content I publish on my site.

Rather than creating a generic chatbot, I wanted something more useful: a chatbot that understands my own content.

That led me to building a **RAG chatbot**.

## What is RAG?

**RAG (Retrieval-Augmented Generation)** is a way of improving AI responses by giving the model access to relevant information before it answers.

Instead of relying only on what the model already knows, it can retrieve specific content from a knowledge base and use that as context when generating a response.

In my case, that knowledge base is my portfolio content:
- My About page  
- My blog posts  
- Future content I publish on the site  

This means the chatbot can answer questions based on what I have actually written, rather than making assumptions or generating generic responses.

## Choosing a Platform

To build the chatbot, I used **Dify**, a platform for building AI applications with support for:
- Large language models
- Knowledge bases
- Embeddings
- Retrieval pipelines
- Easy deployment

I configured the chatbot using:
- **GPT-4o Mini** as the language model
- Embedding models for semantic search
- Reranking for improved retrieval quality
- A knowledge base connected to my portfolio content

## Integrating It Into My Portfolio

The chatbot is embedded directly into my website as a floating chat widget, making it accessible from every page.

The goal was for it to feel like a natural part of the portfolio rather than an external tool. I customized its styling to better match the design of the site, using colors and UI elements consistent with my overall portfolio theme.

Now visitors can ask questions like:

- *What technologies does Markus work with?*  
- *What is he currently learning?*  
- *What are his thoughts on AI applications?*  

And the chatbot answers based on the actual content of my website.

## Automating the Knowledge Base

One of the most interesting parts of the project was automating the chatbot’s knowledge.

I set up a **GitHub Actions workflow** that automatically uploads my markdown content to Dify whenever I push updates to GitHub.

That means:

```text
Write blog post → Push to GitHub → Knowledge updates → Chatbot learns new content
```

## What I Learned

One thing I learned during this project is that building a RAG chatbot sounds much more complicated than it actually is — at least once all the pieces click.

At first, the hardest part wasn’t setting up the chatbot itself. Dify made that part surprisingly straightforward. The real challenge was figuring out how to connect everything together in a way that made sense. I ran into problems with syncing content, GitHub Actions not triggering correctly, and making sure new blog posts were actually uploaded to the chatbot’s knowledge base.

Getting the automation working was probably the biggest hurdle. Once I understood how GitHub Actions worked and how it could connect my portfolio content directly to Dify, everything suddenly became much simpler. After that, it turned into a system that more or less manages itself.

I also learned that small technical details matter a lot. Something as simple as a wrong file path or a typo in a workflow script was enough to stop the entire sync process. Debugging those issues taught me a lot about automation and how different services connect behind the scenes.

Overall, the biggest takeaway is that AI integration doesn’t have to be overly complex. Once the setup is in place, it becomes surprisingly simple to maintain.

## Conclusion

Now that everything is set up, the best part is that I don’t really have to think about it anymore.

Whenever I write a new blog post and push it to GitHub, GitHub Actions automatically uploads it to Dify, updates the chatbot’s knowledge, and makes that content available for future conversations. That means the chatbot grows together with my portfolio without any manual work from me.

What started as a small experiment turned into something I’m genuinely proud of. It’s a practical use of AI, it improves my portfolio, and it gave me hands-on experience with building a real AI-driven application.

And honestly — now that I understand how it works — it feels surprisingly simple.