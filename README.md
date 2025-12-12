# *AI-Powered Fact-Checker Using Gemini 2.0 + Tavily Web Search*

- [Link](https://github.com/aditya230302/GEN_AI_Fact_Checker_and_PDF_based_RAG/blob/main/Fact_Checker.ipynb)

This project implements a **real-time AI fact-checking system** powered by **Google Gemini 2.0** and **Tavily Search API**. Users can input any claim, and the system automatically:

1. **Searches the web** for evidence using Tavily
2. **Extracts and structures the top results**
3. **Sends evidence + claim to Gemini 2.0**
4. **Generates a professional fact-checker style report**
5. Provides:

   * ✔ **Verdict** (True / False / Partially True / Unverified / Outdated)
   * ✔ **Confidence Level**
   * ✔ **Explanation**
   * ✔ **Key Evidence Summary**
   * ✔ **List of all URLs used**

### 🔧 Key Features

* **Automated Web Evidence Retrieval:**
  Utilizes Tavily advanced search to gather unbiased, multi-source evidence.

* **LLM-Based Fact-Verification:**
  Gemini analyzes claims + evidence to deliver structured fact-check results.

* **Interactive CLI Tool:**
  Allows continuous fact-checking in a loop with graceful exits.

* **Robust Error Handling:**
  Handles missing data, API errors, and empty claims.

* **Modular Architecture:**
  Clear separation of functions: search, analysis, display, CLI.

### 🧠 Example Workflow

User enters a claim → Tavily fetches evidence → Gemini analyzes → Verdict returned with full reasoning.

This system can be applied to:
✔ misinformation detection
✔ educational tools
✔ research validation
✔ journalism support
✔ automated moderation pipelines

---

# Private Document-QA System using RAG + Local LLaMA + LangChain

- [Link](https://github.com/aditya230302/GEN_AI_Fact_Checker_and_PDF_based_RAG/blob/main/LangChain_%2B_LLaMA_%2B_PDF_based_RAG.ipynb)

This project implements a **fully local Retrieval-Augmented Generation (RAG) system** using **LLaMA.cpp**, **LangChain**, and **MiniLM embeddings** to process, understand, and answer questions from uploaded PDF documents. The entire pipeline runs **offline**, ensuring privacy and security for sensitive data such as medical reports.

### 🔧 Key Features

* **Local LLaMA Inference (GGUF models via LlamaCpp)**
  Runs a quantized 3B instruction-tuned model efficiently on CPU/GPU using llama.cpp.

* **PDF Parsing & Chunking**
  Utilizes `PyPDFLoader` to convert uploaded PDFs into structured text for retrieval.

* **Vector Embeddings & Semantic Search**
  Generates dense vectors using MiniLM and stores them in `DocArrayInMemorySearch` for lightning-fast retrieval.

* **RAG Pipeline with LangChain**
  Retrieval → Prompt Construction → LLaMA Generation → Output Parsing.

* **Custom Guardrails System**
  Ensures safety, quality, and reliability by:

  * Blocking unsafe keywords
  * Preventing hallucinations
  * Enforcing length constraints
  * Handling empty or malformed responses

* **Performance Benchmarks**
  Measures inference time for both simple and complex semantic queries.

---

# Intelligent Travel Itinerary Generator (Gemini + Tavily API)

- [Link](https://github.com/aditya230302/GEN_AI_Fact_Checker_and_PDF_based_RAG/blob/main/Travel_Buddy.ipynb)

This project implements an **AI-powered travel planning assistant** that generates **personalized itineraries** using **Google Gemini 2.0 Flash** for reasoning and **Tavily Search API** for real-time destination research.
The system collects user preferences such as **destination, budget, duration, interests, and travel style**, fetches fresh travel data from the web, and produces a **fully customized multi-day itinerary**, including safety information, food availability, cultural tips, and emergency contacts.

### 🔧 Key Features

* **Dynamic User Preference Collection:**
  Captures destination, duration, budget, interests, and travel style.

* **Real-Time Destination Research (Tavily API):**
  Automatically gathers up-to-date information on attractions, safety, weather, budget expectations, and travel advisories.

* **LLM-Powered Itinerary Generation (Gemini 2.0):**
  Produces a detailed, human-like travel plan with:

  * Destination overview
  * Cultural & safety guidelines
  * Day-by-day itinerary
  * Food recommendations (veg & non-veg)
  * Emergency contacts

* **Hallucination Reduction:**
  Uses retrieved research data as grounding context so the AI’s output stays factual and not invented.

* **Interactive CLI Travel Assistant:**
  Built with a loop-based interface allowing multiple travel plans in one session.

* **Option to Save Itinerary to File:**
  Users can export the entire travel plan as a `.txt` file.

### 🧠 How It Works

1. User inputs preferences
2. Assistant sends multiple queries to Tavily
3. Aggregates & structures the research
4. Sends all gathered data to Gemini
5. Gemini generates a complete itinerary
6. User can view, customize, or save the plan

This system acts like a **personal AI travel concierge**, combining live web knowledge with high-quality LLM reasoning.

