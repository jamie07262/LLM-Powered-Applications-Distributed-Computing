# LLM-Powered Applications & Distributed Computing

## Overview

The assignment implements an intelligent query system that integrates:

- Big Data Processing (PySpark)
- Retrieval-Augmented Generation (RAG)
- LLM-based Query Routing and Handling

The system is capable of:

1. Answering structured data queries using Spark SQL
2. Answering document-based queries using a RAG pipeline
3. Handling hybrid queries combining both approaches

## Structured Data

1. **Yellow Taxi Trip Data (January 2024):**  
   https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2024-01.parquet

## Document Corpus

The document corpus for this assignment consists of seven publicly available PDF documents related to New York City transportation, taxi operations, transit policy, and urban mobility. These documents were selected to support the Retrieval-Augmented Generation (RAG) component by providing both official policy context and research-based analysis relevant to the NYC Yellow Taxi dataset.

1. **Connecting to the Core: Safer, Greener, and More Convenient Access to the Manhattan Central Business District:**
   An official NYC Department of Transportation planning document that presents projects and strategies for improving sustainable access, mobility, and street design in Manhattan’s central business district.

2. **Investigating Taxi and Uber Competition in New York City: Multi-Agent Simulation by Reinforcement-Learning:**
   An academic research paper that examines competition between yellow cabs, green cabs, and Uber in NYC, focusing on market segmentation, regulations, and demand response through simulation.

3. **New York City Taxi and Limousine Commission 2025 Annual Report:**
   An official TLC annual report summarizing agency operations, fleet statistics, regulations, accessibility progress, enforcement activity, and major policy developments in 2025.

4. **NYC Streets Plan Update 2026:**
   An official NYC DOT update reporting progress on street redesign goals, including protected bus lanes, bike lanes, pedestrian safety improvements, transit enhancements, and Vision Zero outcomes.

5. **Office of Financial Stability Annual Report 2024:**
   A TLC report focused on the economic condition of the yellow taxi medallion industry, including farebox revenue, medallion transfers, debt relief programs, accessibility mandates, and owner support initiatives.

6. **ONE SIZE FITS NONE: MODELING NYC TAXI TIPS:**
   A research paper using 2024 NYC taxi trip data and machine learning to study tipping behavior, showing that yellow taxis and app-based ride services have very different predictive patterns.

7. **TLC Trip Records User Guide:**
   An official technical guide explaining TLC trip record datasets, including yellow taxi, green taxi, and for-hire vehicle data, with details on schema, download sources, taxi zones, and data limitations.

This corpus provides a balanced mix of official government reports, policy and planning documents, dataset documentation, and academic research papers, making it suitable for answering both factual transportation-policy questions and broader analytical questions about NYC taxi operations, regulation, and urban mobility.

## Model Used

- Initially used llama3.3-70b-instruct from course site
- Switched to meta-llama/llama-3.3-70b-instruct from OpenRouter due to credits fully used

## System Architecture

The system consists of three main components:

### 1. Query Router

- Classifies user queries into:
  - DATA
  - DOCUMENT
  - HYBRID
- Outputs structured JSON

### 2. Data Query Handler

- Converts natural language → SQL query
- Executes query using PySpark
- Returns structured results
- Includes retry mechanism for failed queries

### 3. RAG Pipeline

- Uses document embeddings for retrieval
- Generates responses using LLM
- Supports metadata-enhanced chunking

### 4. End-to-End Pipeline

- Routes query → appropriate handler
- Combines outputs (for hybrid queries)
- Returns final response

---

## Technologies Used

- PySpark – Big data processing
- Spark SQL – Query execution
- LangChain – LLM orchestration
- ChromaDB – Vector database
- Sentence Transformers – Embeddings
- Hugging Face Models
- Python 3.11.9
- Java 17

---

## Setup Instructions

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd project
```

2. Create virtual environment

```bash
python -m venv venv
```

Activate:

Windows

```
venv\Scripts\activate
```

Mac/Linux

```
source venv/bin/activate
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

Run Individual Components

- Query Router → classification testing
- Data Handler → SQL execution
- RAG Pipeline → document Q&A

---

## To Run Performance Optimization Section locally

- Ensure you have Hadoop Binaries and set HADOOP_HOME environment variable to enable Spark to carry out file operations
