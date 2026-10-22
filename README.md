# Build a Wealth Management Agentic AI Chatbot with MS Fabric

The aim of this project is to build an Agentic AI-powered Risk Assessment Agent that dynamically analyzes financial data, evaluates investment risks, and provides personalized risk mitigation strategies.

## Overview
This project marks the second phase of the Microsoft Fabric Project to Build a Financial Reporting Agent, introducing Agentic AI to enhance financial data analysis, risk assessment, and investment planning. While the first phase of the project focused on centralizing wealth management data using Microsoft Fabric, this phase transforms the system into an intelligent financial assistant that can autonomously analyze data, generate investment strategies, and provide dynamic risk assessments. By incorporating Agentic AI, the system dynamically selects the best financial tools and executes complex multi-step workflows based on user intent.

## Data
The dataset includes comprehensive financial information crucial for wealth management:

1. Wealth Assets Data: Details of client portfolios, including asset classes such as stocks, bonds, real estate, and alternative investments.
2. Financial Records: Transaction histories, and investment portfolios for a complete financial overview.

_Data is not included in this repository._

## Approach
1. Defining the Goal and Task Decomposition

- Establish the core objective: Assess financial risks and provide mitigation strategies.
- Break down the goal into smaller, manageable tasks: ○ Analyze stock positions and portfolio distribution. ○ Identify and quantify risk exposure (e.g., market volatility, diversification gaps). ○ Generate tailored risk mitigation strategies. ○ Refine recommendations based on user feedback.

2. Building the Agentic AI Framework

- Develop an AI agent that autonomously selects and executes financial analysis tools.
- Use Chain of Thought (CoT) reasoning to dynamically determine the best approach for risk assessment.
- Implement task selection to optimize decision-making.

3. Creating Modular Financial Analysis Tools

- Stock Position Analysis Tool: ○ Retrieves user’s portfolio composition from the database. ○ Assesses market volatility and stock performance.
- Risk Calculation Tool: ○ Calculates portfolio exposure, diversification levels, and historical risk trends. ○ Evaluates risk-to-reward ratios for different asset classes.
- Risk Mitigation Suggestion Tool: ○ Suggests portfolio reallocation, hedging strategies, or alternative investments. ○ Adapts recommendations based on user goals (e.g., conservative vs. aggressive investor).
- Feedback Loop & Refinement Tool: ○ Captures user responses to previous recommendations. ○ Refines future risk assessments based on historical interactions.

4. Implementing Memory Management & Context Retention

- Store user financial history and past recommendations using a vector database.
- Enable agent to recall previous interactions and maintain personalized, context-aware conversations.

5. Developing the Decision-Making Logic

- Implement Intent Detection to classify queries into:

○ Risk Analysis (e.g., "How risky is my portfolio?"). ○ Investment Planning (e.g., "What are safe investments for me?"). ○ Unknown Queries (fallback mechanism for unrelated questions).
- Use the agent to decide which tool(s) should dynamically execute.

6. Create a Flask-Based API

- Develop an API endpoint that accepts user queries and routes them to the AI agent.
- Pass user inputs, retrieve responses from AI tools, and store conversation history.
- Integrate a HTML frontend chatbot to interact with the risk assessment system in real time.

Modular code overview:

## Tech stack
➔ Language: Python 3.10 ➔ Libraries: pandas, numpy, Azure, langchain, Open AI, Flask ➔ Cloud Platform Components: Microsoft Fabric (OneLake, LakeHouse, Fabrics Datawarehouse) ➔ Model: Retrieval-Augmented Generation (RAG) with GPT ➔ Cloud Platform: Azure ➔ API Framework: Flask API with HTML UI

## How to run
```bash
pip install -r Code Folder/requirements.txt
python Code Folder/app.py
```

## Project structure
```
.gitignore
Code Folder/
  Agent/
    __init__.py
    agent.py
    intent.py
    memory.py
    tools.py
  CreateDataWarehouse/
    CreatingTables.sql
    InsertToSQL.py
  FinancialGoals/
    RAGToSQL/
  app.py
  connection.py
  readme.md
  requirements.txt
  templates/
    index.html
README.md
```

## Credits
Based on a ProjectPro guided project.
