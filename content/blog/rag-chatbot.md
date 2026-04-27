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