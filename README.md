<div align="center">

<img src="logo.png" alt="Netflix Logo" width="420">

# 🎬 Netflix Data Analysis — SQL Project

<p align="center">
  <a href="https://ilikemanish.github.io/Netflix-SQL-Data-Analysis/">
    <img src="https://img.shields.io/badge/🚀%20LIVE%20INTERACTIVE%20PREVIEW-E50914?style=for-the-badge&logo=netflix&logoColor=white" alt="Live Interactive Preview">
  </a>
</p>

### 📊 15 Business Problems & SQL Solutions using PostgreSQL

![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL](https://img.shields.io/badge/Language-SQL-orange?style=for-the-badge&logo=postgresql&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Project-Data%20Analysis-green?style=for-the-badge)
![Netflix](https://img.shields.io/badge/Domain-Netflix%20Content-E50914?style=for-the-badge&logo=netflix&logoColor=white)

</div>

---

# 📌 Project Overview

This project is a **Netflix Content Analysis SQL Project** developed using **PostgreSQL**.

The analysis explores Netflix movies and TV shows to answer **15 practical business questions** related to content types, ratings, release years, countries, genres, directors, actors, seasons, and content descriptions.

The project demonstrates how SQL can be used to transform raw entertainment data into meaningful analytical insights.

---

# 🎯 Project Objectives

The main objectives of this project are to:

- 🎬 Analyze Movies vs TV Shows
- ⭐ Identify the most common ratings
- 📅 Analyze content by release year
- 🌍 Find countries producing the most content
- ⏱️ Identify the longest movies
- 🆕 Find recently added content
- 🎥 Analyze content by directors
- 📺 Find TV shows with multiple seasons
- 🏷️ Analyze content by genre
- 🇮🇳 Analyze India's Netflix content
- 📚 Identify documentary movies
- ❌ Find content without director information
- 🎭 Analyze appearances of specific actors
- 👥 Find top actors in Indian content
- 🔎 Categorize content using description keywords

---

# 📁 Dataset Information

| Attribute | Details |
|---|---|
| 🎬 Dataset | Netflix Titles |
| 🗄️ Database | PostgreSQL |
| 💻 Language | SQL |
| 📊 Analysis Type | Exploratory & Business Analysis |
| 📌 Total Problems | 15 |
| 🌍 Domain | Entertainment / Streaming |
| 🛠️ Tool | PostgreSQL / pgAdmin |

---

# 🗂️ Database Schema

The project uses a single main table:

### `Netflix`

| Column | Description |
|---|---|
| `show_id` | Unique content ID |
| `type` | Movie or TV Show |
| `title` | Content title |
| `director` | Director name(s) |
| `casts` | Actor/cast information |
| `country` | Country/countries associated with the content |
| `date_added` | Date content was added to Netflix |
| `release_year` | Original release year |
| `rating` | Content rating |
| `duration` | Movie duration or TV show seasons |
| `listed_in` | Genre/category information |
| `description` | Content description |

---

# 🛠️ Tools & Technologies

- 🐘 **PostgreSQL**
- 💻 **SQL**
- 🖥️ **pgAdmin**
- 📊 Aggregate Functions
- 🔗 SQL String & Array Functions
- 🪟 Window Functions
- 📅 Date Functions
- 🔍 Filtering & Sorting
- 🧩 CTEs
- 📈 Business Analysis

---

# 📊 15 Business Problems

## 1️⃣ Movies vs TV Shows

**Question:** Count the number of Movies and TV Shows available on Netflix.

**Concepts:** `GROUP BY`, `COUNT()`

---

## 2️⃣ Most Common Rating

**Question:** Find the most common rating for Movies and TV Shows separately.

**Concepts:**
- CTE
- `COUNT()`
- `RANK()`
- Window Functions
- `PARTITION BY`

---

## 3️⃣ Movies Released in a Specific Year

**Question:** List all movies released in **2020**.

**Concepts:** `WHERE`, filtering

---

## 4️⃣ Top 5 Countries by Content

**Question:** Find the top 5 countries associated with the highest number of Netflix content items.

**Concepts:**
- `STRING_TO_ARRAY()`
- `UNNEST()`
- `GROUP BY`
- `ORDER BY`
- `LIMIT`

---

## 5️⃣ Longest Movie

**Question:** Identify the movie with the longest duration.

**Concepts:**
- `SPLIT_PART()`
- Type casting
- `ORDER BY`

---

## 6️⃣ Content Added in the Last 5 Years

**Question:** Find Netflix content added within the last 5 years based on the current date.

**Concepts:**
- `TO_DATE()`
- `CURRENT_DATE`
- `INTERVAL`
- Date filtering

---

## 7️⃣ Content by Director

**Question:** Find all movies and TV shows associated with the director **Rajiv Chilaka**.

**Concepts:**
- `STRING_TO_ARRAY()`
- `UNNEST()`
- Subquery
- Filtering

---

## 8️⃣ TV Shows with More Than 5 Seasons

**Question:** List all TV Shows having more than 5 seasons.

**Concepts:**
- `SPLIT_PART()`
- Type casting
- Multiple conditions

---

## 9️⃣ Content by Genre

**Question:** Count the number of Netflix content items in each genre.

**Concepts:**
- `STRING_TO_ARRAY()`
- `UNNEST()`
- `COUNT()`
- `GROUP BY`

---

## 🔟 India's Content Release Analysis

**Question:** Find the yearly Netflix content releases associated with India and return the top 5 years based on the calculated percentage of India's total content.

**Concepts:**
- `GROUP BY`
- Subquery
- `COUNT()`
- Percentage calculation
- `ORDER BY`
- `LIMIT`

> **Note:** The SQL solution calculates a percentage (`avg_release`) representing each year's share of the total India-associated content; it is not a statistical average.

---

## 1️⃣1️⃣ Documentary Movies

**Question:** List all movies categorized as documentaries.

**Concepts:** `LIKE`, filtering

---

## 1️⃣2️⃣ Content Without a Director

**Question:** Find all Netflix content where director information is missing.

**Concepts:** `IS NULL`

---

## 1️⃣3️⃣ Salman Khan — Last 10 Years

**Question:** Find Netflix content featuring **Salman Khan** released within the last 10 years.

**Concepts:**
- `LIKE`
- `EXTRACT()`
- Date/year filtering

---

## 1️⃣4️⃣ Top 10 Actors in Indian Content

**Question:** Find the top 10 actors appearing in the highest number of content items associated with India.

**Concepts:**
- `STRING_TO_ARRAY()`
- `UNNEST()`
- `COUNT()`
- `GROUP BY`
- `ORDER BY`
- `LIMIT`

---

## 1️⃣5️⃣ Description-Based Content Categorization

**Question:** Categorize content based on whether the description contains the keywords **"kill"** or **"violence"**.

- Contains either keyword → `Bad`
- Does not contain either keyword → `Good`

Then count the content in each category by type.

**Concepts:**
- `CASE`
- `ILIKE`
- Subquery
- `GROUP BY`
- Conditional logic

> **Important:** The `Good`/`Bad` labels are analytical categories defined by this project based only on keyword presence; they are not official Netflix classifications.

---

# 🧠 SQL Concepts Used

### 🔹 Basic SQL
- `SELECT`
- `WHERE`
- `DISTINCT`
- `GROUP BY`
- `ORDER BY`
- `LIMIT`

### 🔹 Aggregate Functions
- `COUNT()`
- `SUM()`

### 🔹 Advanced SQL
- CTEs
- Subqueries
- Window Functions
- `RANK()`
- `PARTITION BY`
- `CASE`
- `ILIKE`

### 🔹 PostgreSQL Functions
- `STRING_TO_ARRAY()`
- `UNNEST()`
- `SPLIT_PART()`
- `TO_DATE()`
- `EXTRACT()`
- Type Casting
- `INTERVAL`

---

# 📈 Analysis Areas

| Area | Analysis |
|---|---|
| 🎬 Content Type | Movies vs TV Shows |
| ⭐ Ratings | Most frequent ratings |
| 📅 Release | Year-wise content |
| 🌍 Geography | Country-wise content |
| ⏱️ Duration | Longest movies |
| 🆕 Additions | Recently added content |
| 🎥 Directors | Director-based analysis |
| 📺 TV Shows | Season analysis |
| 🏷️ Genres | Genre-wise content |
| 🇮🇳 India | India-related content analysis |
| 🎭 Actors | Actor appearance analysis |
| 🔎 Descriptions | Keyword-based categorization |

---

# 💡 Key Analytical Insights

This project can help analysts explore:

- 📊 The distribution of Movies and TV Shows.
- ⭐ Which ratings occur most frequently by content type.
- 🌍 Countries associated with large volumes of Netflix content.
- ⏱️ The longest movies in the dataset.
- 🆕 Content added during a recent five-year period.
- 📺 TV shows with more than five seasons.
- 🏷️ Genre-level content distribution.
- 🇮🇳 Year-wise content associated with India.
- 🎭 Actor appearances within the dataset.
- 🔎 Description-based keyword patterns.

---

# 📂 Repository Structure

```text
Netflix-SQL-Analysis/
│
├── README.md
│
├── logo.png
│
├── SQL/
│   └── Solutions of 15 business problems.sql
│
└── Documentation/
    └── Netflix_SQL_Project.pdf
```

> You can rename the SQL file to `Netflix_SQL_Analysis.sql` for a cleaner GitHub repository structure.

---

# 🚀 How to Run the Project

### 1️⃣ Create the Database

Create a PostgreSQL database using **pgAdmin** or the PostgreSQL terminal.

### 2️⃣ Create the Table

Run the `CREATE TABLE Netflix` statement from the SQL file.

### 3️⃣ Import the Dataset

Load the Netflix dataset into the `Netflix` table.

### 4️⃣ Run the Queries

Execute the 15 business-problem queries one by one in PostgreSQL.

### 5️⃣ Explore the Results

Review the query outputs to understand Netflix content patterns.

---

# 📄 Project Files

### SQL File
`Solutions of 15 business problems.sql`

Contains:

- Table creation
- Data inspection queries
- 15 business problems
- SQL solutions

### Documentation
`Netflix_SQL_Project.pdf`

Can be used to present the business questions, queries, and analysis.

---

# 🎓 Skills Demonstrated

- SQL Data Analysis
- PostgreSQL
- Data Cleaning Concepts
- Exploratory Data Analysis
- Business Problem Solving
- Aggregation & Filtering
- Advanced SQL
- Window Functions
- String & Array Processing
- Date Analysis
- Analytical Thinking

---

# 👨‍💻 Author

**Manish Kashyap**

🎯 Aspiring Data Analyst  
📊 SQL | Excel | Python | Data Analytics  
🤖 AI & ML Enthusiast

---

<div align="center">

### ⭐ If you find this project useful, consider giving the repository a star!

**Built with SQL & PostgreSQL 💻📊**

</div>
