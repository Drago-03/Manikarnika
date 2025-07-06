# 🛰️ AI-based Help Bot for Information Retrieval from a Knowledge Graph  
### Powered by NLP, RAG, and Knowledge Graph on the MOSDAC Portal  

---

## 📖 Overview

The **MOSDAC** portal (www.mosdac.gov.in) hosts extensive satellite data, documentation, FAQs, and services. Despite its rich dataset, users often struggle to access the right information due to layered navigation, static formats, and lack of semantic search.

This project proposes an **AI-powered Help Bot** that intelligently ingests all content (static & dynamic) and answers user queries via a **natural language interface**. It uses **Retrieval-Augmented Generation (RAG)** and a **Knowledge Graph** for contextual and relationship-based answers — enabling geospatially aware, multi-turn conversations.

---

## 🧠 Objectives

- 🧠 Develop an NLP/ML-based intelligent virtual assistant.
- 🌐 Parse unstructured/structured web content into a dynamic knowledge graph.
- 📍 Support geospatial data intelligence in queries.
- 🧭 Enable relationship/context-aware discovery.
- 🧩 Ensure modularity for reuse across other ISRO/Indian portals.

---

## 🎯 Expected Outcomes

- 🤖 A conversational help bot that answers public queries on the MOSDAC portal.
- 🌐 A knowledge graph that maps entities and relationships across portal data.
- 🔁 Modular AI stack that can be adapted to other ISRO and research websites.

---

## 🔍 Opportunity & Differentiation

### ❌ Problem with Existing Systems:
- Poor navigation and discoverability.
- Traditional keyword-based search with no semantic/contextual awareness.
- Inability to understand intent, link entities, or manage conversational context.

### ✅ Our Unique Solution:
- Uses **NLP + RAG + Knowledge Graphs** for precise semantic understanding.
- Understands **natural language questions**, not just keywords.
- Handles **multi-format content** (PDFs, tables, metadata, ARIA tags).
- Includes **geospatial awareness** for region/time-based queries.
- Designed to be **modular and plug-and-play** for other data portals.

---

## 🌟 Key Features

| Feature | Description |
|--------|-------------|
| 🔍 Natural Language Interface | Ask complex questions in plain English. |
| 🌐 Knowledge Graph Mapping | Maps mission → satellite → product → data. |
| 📍 Geospatial Query Support | Understands location-based and temporal queries. |
| 🧾 Multi-format Parsing | Works with PDF, DOCX, XLSX, HTML, metadata, and more. |
| 🧠 Retrieval-Augmented Generation | Contextual generation from knowledge base. |
| 💬 Conversational Chat Interface | Memory-based multi-turn interaction. |
| 🧩 Modular Plugin Architecture | Deployable on other ISRO/NIC portals. |

---

## 📊 Process Flow

```mermaid
flowchart TD
    A[User Query] --> B[Intent & Entity Recognition]
    B --> C[Query Parser (LLM/NLP)]
    C --> D[Knowledge Graph Access Layer]
    C --> E[Document Retriever (RAG Embedding)]
    D --> F1[Structured Answer Generator]
    E --> F2[LLM-based Contextual Generator]
    F1 --> G[Response Ranker & Synthesizer]
    F2 --> G
    G --> H[Chatbot UI]
```

## 📘 Use-Case Flow

```mermaid
graph LR
    U[User] -->|Asks "Where can I find rainfall data for Mumbai?"| Q1[NLP Module]
    Q1 -->|Extract Intent: Data Retrieval| K1[Knowledge Graph Query]
    Q1 -->|Retrieve Relevant Docs| RAG1[Context Retriever]
    K1 --> RES1[Structured Data]
    RAG1 --> RES2[Unstructured Data]
    RES1 --> BOT[Response Engine]
    RES2 --> BOT
    BOT --> U
```

## 🏗️ Architecture

```mermaid
graph TD
    subgraph Frontend
        A1[React / Streamlit Chat UI]
    end

    subgraph Backend Services
        B1[NLP Layer (spaCy, NLTK)]
        B2[Intent Classifier + Entity Extractor]
        B3[RAG Retriever (LangChain, FAISS, NVIDIA RAG)]
        B4[Document Store (ChromaDB / Weaviate)]
        B5[Knowledge Graph Engine (Neo4j/RDFStore)]
        B6[Contextual Answer Synthesizer (LLM like LLaMA2 / GPT-4)]
    end

    subgraph Crawler & Preprocessing
        C1[Custom Web Crawler (HTML, ARIA, Metadata)]
        C2[PDF/DOCX Parser (pdfminer, textract)]
        C3[Table Extractor (Camelot)]
        C4[Satellite Metadata Extractor]
    end

    A1 --> B1
    B1 --> B2
    B2 --> B3
    B2 --> B5
    C1 --> B3
    C2 --> B3
    C3 --> B3
    B3 --> B4
    B5 --> B6
    B4 --> B6
    B6 --> A1
```

## 🛠️ Technologies Used

| Layer               | Tools                                  |
| ------------------- | -------------------------------------- |
| Frontend            | React.js / Streamlit                   |
| Backend             | Node.js / FastAPI (Python)             |
| NLP/ML              | spaCy, NLTK, Sentence-BERT             |
| RAG                 | LangChain, FAISS, ChromaDB, NVIDIA RAG |
| Knowledge Graph     | Neo4j / RDFLib                         |
| Crawling & Parsing  | BeautifulSoup, Scrapy, Selenium        |
| Document Extraction | pdfminer, textract, docx2txt, Camelot  |
| Geospatial          | GeoPandas, rasterio, GDAL              |
| Deployment          | Docker, AWS, Nginx                     |


## 🧱 Wireframes (Described)

Landing Page:
Search bar with “Ask me anything about MOSDAC...”
Button for documentation and query examples
Conversation Interface:
Left: Chat flow (messages, suggestions)
Right (optional): Knowledge Graph visualizations or satellite info
Admin Panel (Optional):
Upload documents, FAQs
Review misinterpreted queries for retraining

## ✅ Evaluation Metrics

| Metric                         | Description                                            |
| ------------------------------ | ------------------------------------------------------ |
| 🎯 Intent Recognition Accuracy | Correct detection of user intent                       |
| 🧠 Entity Recognition Accuracy | Precision in identifying data fields, places, missions |
| 📚 Response Completeness       | Coverage of answer relative to the question            |
| 🔁 Context Retention           | Quality of multi-turn conversations                    |
| ⚙️ System Modularity           | Ease of deploying on other portals                     |


## 🔚 Summary

This intelligent help bot leverages cutting-edge NLP and RAG architectures to make scientific satellite data more accessible. Designed for MOSDAC, but scalable across portals like Bhuvan, NRSC, VEDAS, and more — this solution empowers researchers, students, and citizens alike.
