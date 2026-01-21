# AgriTech: Direct Farmer-to-Restaurant Marketplace

National Innovation Challenge - IdeaSprint '26 | GPREC Coders' Club

Problem Statement:

Farmers often face low profits due to multiple intermediaries taking significant margins, while restaurants pay higher prices. This marketplace connects **Farmers directly to Restaurants**, providing real-time price visibility and a RAG-powered AI assistant to demystify complex agricultural policies and contracts.

Key Features:

* **Direct Marketplace:** A platform for transparent transactions between producers and buyers.
* **Privacy-First RAG Chatbot:** An AI assistant that answers queries using local knowledge without external API calls.
* **Logistics Automation:** Streamlined scheduling for produce delivery.
* **Zero-Cost Infrastructure:** Built entirely on open-source tools to ensure the solution is free to scale.

Local RAG Architecture (Compliance):

To follow the **No Third-Party API** rule, our system implements a **Retrieval-Augmented Generation (RAG)** pipeline locally:

1. **Knowledge Base:** Uses the "Guidelines Farm Services Act 2020" text file as the source of truth.
2. **Retrieval:** The backend reads relevant sections of the local document based on user queries.
3. **Local LLM:** We use **Ollama** with the **Llama 3.2:1b** model to generate responses on-device, ensuring 100% data privacy and zero API costs.

Tech Stack:

* **Backend:** Node.js + Express
* **AI Engine:** Ollama (Local LLM)
* **Data Management:** Local File System (fs) for document indexing
* **Language:** JavaScript

Setup & Installation:

Follow these steps to run the project locally:

1. **Clone the Repository:**

git clone https://github.com/codecrew404-lgtm/AgriTech-Direct-Marketplace.git



2. **Install Dependencies:**
bash
npm install




3. **Setup Ollama:**
* Install Ollama from [ollama.com](https://ollama.com).
* Run `ollama pull llama3.2:1b` in your terminal.


4. **Start the Server:**

npm start




