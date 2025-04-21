# multi_agent_system_ds_team
Experimental project to create a multi-agent AI system for a data analysis team

Description

This project implements a Multi-Agent System for data analysis teamn. The system simulates a team of agents, each responsible for specific steps in the data analysis pipeline, including question interpretation, dataset selection, model suggestion, data storytelling, and coordination of final output. The agents are powered by OpenAI's GPT-3.5 and use memory to improve the quality of interactions and task completion over time.

This system is designed to help automate the process of data analysis by mimicking how human teams collaborate on data science projects. It leverages the power of Large Language Models (LLMs) to simulate different roles in a data analysis workflow.

Agents Overview

Attendant Agent: Responsible for interpreting the customer's query and rephrasing it clearly for the data analyst.

Data Analyst Agent: Searches for relevant datasets (e.g., on Kaggle) or suggests synthetic datasets for the problem at hand.

Data Scientist Agent: Proposes an appropriate machine learning model based on the dataset and the problem's requirements.

Storyteller Agent: Creates a narrative summary of the analysis, making it accessible and clear to non-technical stakeholders.

Coordinator Agent: Organizes the workflow, ensuring that all tasks are completed in the right order and consolidates the final response to the customer.

Technologies Used

OpenAI GPT-3.5: Provides the LLMs that power each agent.

LangChain: Used to create the framework for agent orchestration and task management.

CrewAI: Orchestrates the workflow by coordinating tasks between agents.

Memory Buffer: Each agent has a memory component to maintain conversation context and improve task execution over time.

Setup Instructions

Prerequisites

Python 3.7 or higher
pip for managing dependencies

Installation
Clone the repository:

git clone https://github.com/FelipeBrusse/multi_agent_system_ds_team.git
cd multi-agent-data-analysis

Install the required dependencies:

pip install -r requirements.txt

Set up your OpenAI API key in the code (OPENAI_API_KEY).

Run the main.py file to start the system:

python main.py

Example Usage

workflow_with_memory("What is the best ML model to classify flowers?")

The system works by receiving a user's question and routing it through a series of tasks. Here's an example of how the system processes a query:

workflow_with_memory("What is the best ML model to classify flowers?")

Project Structure

.
├── agents/
│   ├── attendant_agent.py
│   ├── analyst_agent.py
│   ├── data_scientist_agent.py
│   ├── storyteller_agent.py
│   └── coordinator_agent.py
├── utils/
│   ├── memory.py
│   ├── tasks.py
│   └── workflow.py
├── requirements.txt
└── main.py

How It Works

The system orchestrates the flow of tasks between agents, ensuring each agent performs its role in sequence. Each agent has its own memory to store context from previous interactions. The memory improves the system's ability to provide accurate responses by retaining relevant details across tasks.

Attendant Agent: Receives the user's question and reformulates it into a clear query for the Data Analyst Agent.

Data Analyst Agent: Searches for the most suitable dataset (from Kaggle or synthetic datasets) and provides the information to the Data Scientist Agent.

Data Scientist Agent: Analyzes the problem and recommends a machine learning model based on the dataset.

Storyteller Agent: Summarizes the analysis and insights in an easily understandable format for non-technical users.

Coordinator Agent: Consolidates all the outputs and presents the final response to the user.

Future Improvements
Multi-Domain Support: Extend the agents to handle different types of data analysis (e.g., NLP, image classification, time series).

Real-Time Dataset Access: Integrate with more external data sources for real-time dataset fetching.

Improved Memory Management: Enhance memory usage to manage context across multiple sessions.






