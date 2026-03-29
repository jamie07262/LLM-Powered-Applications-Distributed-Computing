# LLM-Powered Applications & Distributed Computing

## Overview

In this assignment, I will use LLM, RAG, and Spark techniques to create an intelligent analytics system. I will process large datasets with Spark and build a RAG pipeline to answer natural language questions using both structured data and document retrieval—mirroring how real organizations combine data analytics with AI search for insights.

## Structured Data

1. **Yellow Taxi Trip Data (January 2024):**  
   https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2024-01.parquet

## Document Corpus

The document corpus for this project consists of seven publicly available PDF documents related to New York City transportation, taxi operations, transit policy, and urban mobility. These documents were selected to support the Retrieval-Augmented Generation (RAG) component by providing both official policy context and research-based analysis relevant to the NYC Yellow Taxi dataset.

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
