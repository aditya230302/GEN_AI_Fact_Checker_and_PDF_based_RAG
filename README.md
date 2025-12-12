# *AI-Powered Fact-Checker Using Gemini 2.0 + Tavily Web Search*

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
