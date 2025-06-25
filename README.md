## Overview

This repository showcases a prototype pipeline for **prompt-based microsite generation**, where large language models (LLMs) are augmented with real-time web search data. The core objective is to produce **concise, promotional microsites** enriched with the latest contextual information, without relying on static or bio-link content.

At the heart of this approach is the integration of the **Serper API**, a fast and lightweight alternative to traditional search engines. It allows the system to **fetch trending, topic-specific web data**, which is then passed to the LLM to ground its responses in current, relevant information using **Retrieval-Augmented Generation (RAG)** techniques.

---

## Notebooks

### 1. `Google_Serper.ipynb`

This notebook demonstrates how **Serper API** is used to retrieve real-time web results based on a user-defined topic or query. The results are cleaned, parsed, and structured to serve as **external context** for the language model. Key functions:

* Query Google-like results using the Serper API.
* Extract concise summaries from the retrieved web pages.
* Combine results into a structured input prompt for the LLM.
* Uses Retrieval-Augmented Generation (RAG) to enrich the content with fresh, relevant information.
* Can be extended or reused for other use cases needing lightweight, real-time search-based context injection.


This ensures that the model's output is **not purely based on its training data**, but rather grounded in **up-to-date, real-world information**, improving factual accuracy and relevance.

---

### 2. `OpenAI_Serper.ipynb.ipynb`

This notebook maps the overall system design and shows how the Serper-enhanced context is used in practical implementation. For each deliverable related to the microsite generation engine, it:

* Demonstrates prompt construction using Serper-derived context.
* Runs LLM completions (e.g., GPT-4o Mini) on the enriched input.
* Outputs finalized microsite content and evaluates how Serper results influenced the generated text.
* A modular breakdown of the "Promote" intent microsite generation flow.
* Descriptions of each functional step, including data inputs, processing logic, and content rendering.
* Output examples and impact assessment derived from the generated microsite conten

This helps illustrate how integrating **search-based grounding** directly impacts the quality, tone, and clarity of the final microsite content.

---

## How to Use

1. Clone this repository and ensure a working Python environment with Jupyter installed.
2. Obtain a Serper API key and insert it into the relevant section of `google_serper_test.ipynb`.
3. Enter a topic of interest to retrieve web results via Serper and pass that context to the LLM.
4. Use `Deleverables.ipynb` to view how this workflow supports specific content generation deliverables.

---

## 🔧 Requirements

* Python 3.8+
* Serper API key ([https://serper.dev/](https://serper.dev/))
* OpenAI-compatible language model (e.g., GPT-4o Mini)
* Dependencies: `requests`, `json`, `IPython.display`, etc.

---

## Use Cases

This system can be adapted for:

* Promotional microsite/landing page creation
* Marketing copy grounded in current trends
* RAG-based summarization or personalization tools
* Use cases where **live context improves LLM output relevance**

