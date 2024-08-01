# Financial News Analytics with Knowledge Graphs and LLM-based Agents

## Overview

This project demonstrates an advanced approach to financial news analytics using knowledge graphs and Large Language Model (LLM) based agents. It showcases how different knowledge graph implementations can augment LLM-driven financial news analysis pipelines with factual data, grounding the results in solid financial knowledge.

## Key Features

- Utilizes both Semantic Web (RDF) and Labeled Property Graph (Neo4j) implementations
- Integrates Anthropic's Claude 3.5 Sonnet for LLM-based analysis
- Demonstrates Retrieval-Augmented Generation (RAG) in financial context
- Provides examples of financial news sentiment analysis

## What Does It Do?

The notebook contains mock financial news examples and corresponding facts in two small graph databases:
1. Apache Jena Fuseki-based TDB2 knowledge graph
2. Neo4j-based Labeled Property Graph

Claude Sonnet-based agents analyze the mock news articles to retrieve sentiment values. These agents access the knowledge graphs to retrieve relevant facts, enhancing the accuracy of their analysis by incorporating fresh, context-specific knowledge.

## Unique Approach

Unlike many knowledge graph-based RAG applications that focus on extracting facts from textual data, this project demonstrates the power of utilizing existing knowledge graphs. These graphs are based on a combination of traditional financial data and manually curated facts typically available at financial institutions. This approach provides more accurate and verified facts compared to scraping public news data, driving the AI model to provide more precise responses.

## Components

The project uses three Docker images:
- Jupyter Notebook: [quay.io/jupyter/base-notebook](https://quay.io/repository/jupyter/base-notebook)
- Neo4j: [neo4j](https://hub.docker.com/_/neo4j)
- Apache Jena Fuseki: [secoresearch/fuseki](https://hub.docker.com/r/secoresearch/fuseki)

## Prerequisites

- Docker and Docker Compose
- Anthropic API key

## Setup and Running

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/financial-news-analytics-kg.git
   cd financial-news-analytics-kg
   ```

2. Add your Anthropic API key to the `.env` file:
   ```
   ANTHROPIC_API_KEY=your_api_key_here
   ```

3. Start the Docker containers:
   ```
   docker compose up -d
   ```

4. Access the Jupyter notebook at:
   ```
   http://localhost:8888
   ```

## Usage

Navigate through the Jupyter notebook to see examples of:
- Financial news analysis
- Knowledge graph querying
- LLM-based sentiment analysis
- Comparison of results with and without knowledge graph augmentation

## License

[MIT License](LICENSE)

## Contact

For questions or feedback, please open an issue in this repository.
