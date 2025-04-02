# Project Title: Graph-Based AI Query System with LangChain and Neo4j

## Overview
This project is a Graph-Based AI Query System utilizing LangChain, Neo4j, and other AI-powered tools. It enables users to interact with a knowledge graph database using natural language queries, leveraging Cypher queries to extract meaningful insights.

## Features
- **Graph Database Integration**: Uses Neo4j for storing and querying structured data.
- **LangChain for AI Processing**: Handles the natural language processing and query conversion.
- **LLM Chain Integration**: Converts user queries into Cypher queries to interact with the Neo4j database.
- **Graph Query Processing**: Supports multiple query types for knowledge retrieval.

## Project Structure
```
├── experiments.ipynb   # Jupyter Notebook for running and testing the project
├── requirements.txt    # Dependencies required for the project
├── README.md           # Project documentation
├── env                 # Environment variables
```

## Installation
### 1. Clone the Repository

### 2. Create a Virtual Environment (Optional but Recommended)

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Set Up Neo4j Database
- Install and set up Neo4j (https://neo4j.com/download/)
- Start Neo4j and set up a database with your credentials.
- Update `config.py` with the following details:
```python
NEO4J_URI = "bolt://localhost:7687"
NEO4J_USERNAME = "neo4j"
NEO4J_PASSWORD = "yourpassword"
```

## Usage
1. **Run the Jupyter Notebook**
```bash
jupyter notebook
```
- Open `experiments.ipynb` and execute the cells.

2. **Run the Main Script**
```bash
python main.py
```

3. **Query the Graph**
- Modify and use `GraphCypherQAChain` in the notebook to interact with the database.
- Example query:
```python
chain.invoke("Which actors played in the movie Casino?")
```

## Dependencies
- Python 3.8+
- Neo4j
- LangChain
- Jupyter Notebook
- Pandas
- dotenv (for environment variables)


### ValidationError: Input should be a valid dictionary
- Ensure your `prompt` input follows the correct format:
```python
prompt = PromptTemplate("How can I help you with {question}?")
```

### CypherSyntaxError: Invalid input in Cypher query
- Check the generated Cypher query before execution.
- Ensure Neo4j is running and properly connected.

## Future Enhancements
- Add support for multiple graph databases.
- Improve LLM chain logic for better query accuracy.
- Integrate additional NLP models for better natural language understanding.
