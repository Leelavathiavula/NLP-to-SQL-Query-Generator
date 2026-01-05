# NLP-to-SQL-Query-Generator

# LLM SQL Query Generator

A **Streamlit-based web application** that converts **natural language questions into SQL queries** using **Google Gemini LLM**, executes them on a **PostgreSQL database**, and displays the results interactively.

This project demonstrates the integration of **LLMs, databases, and web applications** for real-world data querying use cases.

## Project Overview

The LLM SQL Query Generator allows users to:

* Ask questions in **plain English**
* Automatically generate **PostgreSQL-compatible SQL queries**
* Execute queries directly on a database
* View results in a **tabular format**
* Adjust query strictness using **accuracy levels**

It is designed for **students, beginners, and data enthusiasts** who want to query databases without writing SQL manually.


## Tech Stack

* **Python**
* **Streamlit** (Frontend UI)
* **Google Gemini (Generative AI)**
* **PostgreSQL**
* **psycopg2**
* **Pandas**
* **dotenv**


##  Database Schema Used

### STUDENT

* `student_id` (PK)
* `name`
* `branch`
* `skills`
* `cgpa`
* `graduation_year`

### COMPANIES

* `company_id` (PK)
* `name`
* `sector`
* `visit_month`

### OFFERS

* `offer_id` (PK)
* `student_id` (FK → STUDENT)
* `company_id` (FK → COMPANIES)
* `package_lpa`
* `job_role`

##  Key Features

* **English → SQL conversion using LLM**
* **Accuracy tuning**

  * Precise (100%)
  * Balanced (50–90%)
  * Creative (<50%)
* **Automatic salary conversion to LPA**
* **SQL explanation generation**
* **One-click query execution**
* **Results displayed as DataFrame**
*  **Sample queries for easy testing**
*  **Custom UI styling**


##  Accuracy Levels Explained

| Mode                  | Description                                     |
| --------------------- | ----------------------------------------------- |
| **Precise (100%)**    | Generates SQL strictly based on the question    |
| **Balanced (50–90%)** | Allows minimal logical inference                |
| **Creative (<50%)**   | Freely interprets vague or incomplete questions |



## Application Flow

1. User enters a question in English
2. Gemini LLM generates SQL query
3. SQL is extracted and cleaned
4. Query is executed on PostgreSQL
5. Results are shown in Streamlit UI


## Setup Instructions

### 1️⃣Clone Repository

```bash
git clone https://github.com/your-username/llm-sql-query-generator.git
cd llm-sql-query-generator
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Configure Environment Variables

Create a `.env` file:

```env
GOOGLE_API_KEY=your_google_api_key
DB_NAME=your_database_name
DB_USER=your_db_username
DB_PASSWORD=your_db_password
DB_HOST=localhost
DB_PORT=5432
```

### 4️⃣ Run the Application

```bash
streamlit run app.py
```

---

## Sample Queries

* *How many students are in the database?*
* *List students with CGPA above 9*
* *Show job offers above 20 LPA*
* *Find students who are not placed*
* *Top 3 highest package offers with company details*

---

## Learning Outcomes

* Practical use of **LLMs for data querying**
* Integration of **AI + SQL + Web UI**
* Handling **database connections safely**
* Prompt engineering for **controlled LLM output**
* Building real-world **data-driven applications**

---

## Use Cases

* Academic mini / major project
* AI-powered database querying
* Data analytics learning tool
* Resume & GitHub portfolio project


