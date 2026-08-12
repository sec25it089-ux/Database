DataVision AI

Conversational AI for Database Analytics & Visualization


Challenge: Building Intelligent LLM Agents for Database Interaction & Visualization
 

1. Project Overview

DataVision AI is an AI-powered conversational database assistant that allows non-technical users to interact with databases using natural language.

Instead of writing SQL queries manually, users can simply ask questions such as:

«"Show me the top 5 products by revenue."»

DataVision AI understands the request, retrieves the required information from the database, generates an appropriate visualization, and explains the result in simple language.

The project directly addresses the hackathon requirement of building a conversational AI system that connects natural-language queries with databases, visualizations, and data insights.

---

2. The Problem we actually have: 

Modern organizations store large amounts of information in databases. However, accessing this information usually requires knowledge of:

- SQL
- Database schemas
- Tables and relationships
- Data analysis
- Visualization tools

Non-technical users may know what information they need but may not know how to retrieve it.

For example, a business manager may ask:

«"Which products generated the highest revenue this quarter?"»

Normally, a database expert would need to write an SQL query and create a chart.

There is a gap between human questions and technical database operations.

Users should not need to understand SQL just to obtain useful insights from their organization's data.

---

3. Proposed Solution

DataVision AI provides a ChatGPT-like interface for database interaction.

Working Process

User asks a question
        ↓
AI understands the question
        ↓
Database schema is inspected
        ↓
SQL query is generated
        ↓
SQL safety validation
        ↓
Database query execution
        ↓
Result analysis
        ↓
Chart / visualization generation
        ↓
Natural-language explanation
        ↓
User receives the insight

This allows users to interact with complex databases using normal language.

---

4. Example

User

Show the top 5 products by revenue.

DataVision AI

The system:

1. Understands the user's intent.
2. Identifies the required database tables.
3. Generates the required SQL query.
4. Executes the query.
5. Displays the result.
6. Creates a suitable chart.
7. Explains the important insight.

Output

Top products by revenue

Product              Revenue
--------------------------------
Smart Watch           ₹XX,XXX
Wireless Earbuds      ₹XX,XXX
Mechanical Keyboard   ₹XX,XXX
...

The user does not need to write SQL.

---

5. Key Features

5.1 Conversational Chat Interface

A ChatGPT-like interface allows users to communicate with the database through natural-language questions.

5.2 Natural Language to Database Query

Users can ask questions without knowing SQL.

Example:

Which customers placed the most orders?

5.3 Database Schema Discovery

The system can inspect database tables and columns to understand the available data.

5.4 SQL Query Execution

The generated read-only SQL query is executed against the database.

5.5 SQL Safety

The system rejects dangerous database operations such as:

INSERT
UPDATE
DELETE
DROP
ALTER
CREATE

The demonstration system is designed for read-only analytics.

5.6 Automatic Visualization

DataVision AI automatically chooses a suitable visualization.

Supported charts include:

- Bar chart
- Line chart
- Pie chart
- Scatter plot extension

5.7 Data Explanation

The system converts numerical results into understandable insights.

5.8 Database Relationship Visualization

The system can display database schema information and provide an ER-diagram representation.

5.9 Query Transparency

The generated SQL can be viewed by the user, making the system easier to understand and audit.

6. Technology Stack

Frontend

- HTML
- CSS
- JavaScript
- Plotly

Backend

- Python
- FastAPI

Database

- SQLite

The architecture can be extended to:

- MySQL
- PostgreSQL
- MongoDB

AI / Agent Layer

our project is designed to support an LLM-powered agent.

Possible LLM providers include:

- OpenAI
- Google Gemini
- Anthropic Claude
- Open-source LLMs

Visualization

- Plotly
- Mermaid-compatible diagram generation

---

7. Project Structure

DataVisionAI/
│
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── agent.py
│   ├── db.py
│   └── visualizer.py
│
├── data/
│   └── demo.db
│
├── templates/
│   └── index.html
│
├── static/
│   └── style.css
│
├── docs/
│   ├── ARCHITECTURE.md
│   ├── API.md
│   └── DEMO_SCRIPT.md
│
├── seed.py
├── requirements.txt
├── Dockerfile
├── .env.example
├── .gitignore
└── README.md

---

8. Database Used

The demonstration database is an e-commerce database containing:

Customers

customer_id
name
city
segment

Products

product_id
name
category
price

Orders

order_id
customer_id
order_date
status

Order Items

item_id
order_id
product_id
quantity
unit_price

These tables allow the system to demonstrate sales analysis, customer analysis, product analysis, and database relationships.

---

9. Setup Instructions

Step 1 — Clone the Repository
---

Step 2 — Create Virtual Environment

Step 3 — Install Dependencies


Step 4 — Create the Demo Database

Run:

python seed.py

This creates the sample SQLite database.

---

Step 5 — Configure Environment Variables

Create a ".env" file based on:

.env.example

Example:

OPENAI_API_KEY=
OPENAI_MODEL=gpt-4o-mini
DATABASE_PATH=data/demo.db



Step 6 — Start the Application


10. Architecture

                USER
                  |
                  ↓
        Conversational UI
                  |
                  ↓
          AI Agent / Router
                  |
        ┌─────────┼─────────┐
        ↓         ↓         ↓
   Schema Tool  SQL Tool  Diagram Tool
        |         |         |
        ↓         ↓         ↓
    Database  SQL Safety  Visualization
        |         |
        └────┬────┘
             ↓
        Result Analysis
             |
      ┌──────┴──────┐
      ↓             ↓
   Charts       Explanation
      |             |
      └──────┬──────┘
             ↓
        User Response

---

11. Expected Impact

DataVision AI can make database analytics more accessible to:

- Business managers
- Students
- Teachers
- Analysts
- Small businesses
- Non-technical employees

The user can focus on what they want to know instead of how to write the SQL query.

---

12. Team Information

Team Name

INNOVEXA

Team Members

ELAYAJEEVA S
TEJASHREE S
MYTHILEE U
TAMILSELVAN S
MANASA S


our Responsibilities

Team Member| Responsibility
Member 1| AI / Agent Development
Member 2| Backend & Database
Member 3| Frontend / UI
Member 4| Visualization & Diagrams
Member 5| Testing, Documentation & Deployment


---

13. Conclusion

DataVision AI transforms database interaction from a technical SQL task into a natural conversation.

Instead of asking:

«"How do I write the SQL query?"»

the user simply asks:

«"What do I want to know?"»

The AI handles the database interaction, visualization, and explanation.

DataVision AI — Ask your data. Understand your data.
