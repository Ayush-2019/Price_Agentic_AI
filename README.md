# 🔍 Price Agentic AI

An **agent-driven AI system** that discovers online product deals, predicts their true value using fine-tuned models, and surfaces the most compelling bargains through a user-friendly interface.

---

## 🚀 Overview

**Price_Agentic_AI** is an AI-powered multi-agent workflow platform designed to:

🤖 Multi-Agent Architecture

Five specialized AI agents operate collaboratively to discover, evaluate, and surface the best deals:

1️⃣ Deal Discovery Agent

Scans the internet for bargain products using structured queries and scraping tools.
Extracts raw deal data including product title, description, listed price, and source metadata.

2️⃣ Data Extraction & Normalization Agent

Cleans and standardizes scraped data.
Removes promotional noise (e.g., “$200 off”), extracts the actual product price, and formats descriptions for downstream processing.

3️⃣ Product Understanding Agent

Uses LLM reasoning and RAG to deeply analyze the product description.
Identifies specifications, category, brand, and comparable market signals to create a structured product representation.

4️⃣ Price Estimation Agent (QLoRA Fine-Tuned Model)

Predicts the product’s true market value using a model fine-tuned with QLoRA.
Leverages contextual embeddings and learned pricing patterns to generate an estimated fair price.

5️⃣ Deal Scoring & Selection Agent

Compares listed price with predicted true value.
Calculates value gap, ranks deals, and selects the single most compelling bargain.
Triggers user notification through the orchestration layer (GPT-5 and Llama).

This system combines modern AI capabilities including **agent orchestration, QLoRA-fine-tuned models, RAG (Retrieval-Augmented Generation)**, and **Gradio** for workflow visualization and user interaction.

---

## 🧠 Key Features

### 🌐 1. Internet Deal Discovery

Agents continuously search for deals and collect product data from various online sources.

### 🤖 2. AI-Based Price Prediction

* A **custom model fine-tuned using QLoRA** is used to predict expected prices.
* Deals are evaluated against estimated true values instead of just discount amounts.

### 🚦 3. Multi-Agent Workflow

* Five AI agents operate collaboratively to parse, assess, and prioritize deals.
* Agents are **orchestrated through the OpenAI API (GPT-5) and Llama**, enabling complex reasoning and decision logic.

### 📚 4. RAG and LLM Integration

* Retrieval-Augmented Generation enhances contextual understanding from external reference sources.
* Local models like **LLaMA** are incorporated to support efficient embedding search and reasoning.

### 🖥️ 5. Gradio UI

A **Gradio frontend** visualizes the agents’ workflow, displays top deals, and allows users to interact with the system intuitively.

---

---

## 🛠️ How It Works

1. **Deal Collection**

   * Agents scan online sources and pull deal descriptions, pricing, and metadata.
   * Collected data is preprocessed and indexed.

2. **Price Estimation**

   * A QLoRA-fine-tuned model predicts a product’s expected price based on text description, historical data, and context.
   * RAG fetches relevant external knowledge to improve estimation.

3. **Deal Scoring & Selection**

   * Each deal is scored by comparing listed price to the estimated true price.
   * Only deals with a strong value gap (low price vs high estimated value) are considered.

4. **Orchestration with GPT-5**

   * A master workflow agent coordinates the pipeline leveraging the OpenAI API.
   * Agents communicate and update states through structured prompts and tool hooks.

5. **User Interface**

   * Gradio UI displays the top deals and agent reasoning.
   * Users can explore deal summaries and AI-driven insights interactively.

---

## 🧪 Usage

To test or run the system locally:

1. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

2. Start the Gradio UI

3. Navigate to the provided local URL in your browser to view the interface.

> Detailed setup instructions (API keys, model paths, environment configs) should be included

---

## 💡 Contributions

Contributions are welcome! If you’d like to:

* Add new agent capabilities
* Improve price prediction models
* Support more deal sources
* Enhance the UI

…feel free to open an issue or submit a pull request.

---

## 📌 Summary

Price_Agentic_AI is an **agentic price discovery engine** — combining modern AI models, agent orchestration (via GPT-5, llama), and a polished Gradio UI to surface the best product deals online with intelligent price valuation.
