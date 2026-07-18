---
Updated: 2026-07-16
---
# Spreadsheet Basics & SQL

## The Role of Spreadsheets

- **Purpose:** To organize, clean, and perform basic calculations on small-to-medium datasets.
    
- **Key Concept:** Spreadsheets use **Labels (Headers)** to define attributes and **Cells** to store specific values.
    

## Core Spreadsheet Skills (Hands-on Practice)

- **Formatting:**
    
    - Adjusting column widths and text wrapping for readability.
        
    - Using "Bold" to distinguish headers from data.
        
- **Organization:**
    
    - **Sorting:** Use `Data > Sort range` to reorder data based on specific attributes (e.g., sorting by "Siblings"). _Always check "Data has header row" to avoid sorting your labels._
        
- **Analysis:**
    
    - **Formulas:** Use basic arithmetic (e.g., `=C2+C3+C4`) to perform calculations directly within cells.
        

## Reference Summary (The "Why")

- **Why this matters:** This is the "Process" phase of the Data Analysis lifecycle. Before you can analyze data, you must ensure it is structured consistently (e.g., headers are clear, data is sorted) and formatted correctly so that formulas can accurately reference the cells.
## SQL

#### The Core Template

Use this indentation and structure to avoid syntax errors and improve readability.

SQL

```
SELECT
    column_name1,
    column_name2
FROM
    dataset_name.table_name
WHERE
    condition1 AND condition2;
```

#### Key Commands

|**Clause**|**Purpose**|**Key Rule**|
|---|---|---|
|**SELECT**|Choose which columns to retrieve.|Separate multiple columns with a **comma**.|
|**FROM**|Identify the data source.|Use the `dataset.table` format.|
|**WHERE**|Filter the data.|Use **AND**, **OR**, or **NOT** to join multiple conditions.|

### Analyst Best Practices

- **Be Selective:** Only select the columns you actually need. Requesting unnecessary data is inefficient and uses excess system resources.
    
- **Logical Operators:**
    
    - **AND:** All conditions must be true.
        
    - **OR:** At least one condition must be true.
        
    - **NOT:** Excludes specific criteria.
        
- **Formatting:** Always indent your columns under `SELECT` for readability.
## Advanced Basics & Best Practices

### Professional Formatting

- **Indentation & Case:** SQL is not case-sensitive, but using `UPPERCASE` for commands and indenting columns makes code readable for your team.
    
- **Terminators:** Use a semicolon `;` at the end of your query to signal the end of the statement (standard practice).
    
- **Comments:** Use `--` (or `#` in some systems) for single-line notes to explain _why_ you wrote a query. Use `/* ... */` for multi-line explanations.
    
    - _Analyst Tip:_ Always comment on your queries. Future-you will be grateful when reviewing old code.
        

### Advanced Filtering & Selection

- **The Wildcard `*`:** `SELECT *` retrieves every column in a table.
    
    - _Warning:_ Use this sparingly! It can be extremely slow on large databases. Always select specific columns when possible.
        
- **Pattern Matching (`LIKE`):** Use `LIKE 'Ch%'` to find values starting with "Ch". The `%` acts as a wildcard for any number of characters.
    
- **Aliases (`AS`):** Use `AS` to temporarily rename tables or columns for the duration of the query (e.g., `SELECT last_name AS surname`). This makes output reports easier for stakeholders to read.
    

### Logical Operators Summary

|**Operator**|**Meaning**|**Example**|
|---|---|---|
|**`<>` or `!=`**|Does not equal|`WHERE jobCode <> 'INT'`|
|**`AND`**|Both conditions must be met|`WHERE salary <= 30000 AND jobCode <> 'INT'`|
|**`OR`**|At least one condition met|`WHERE salary > 30000 OR jobCode = 'MGR'`|

### Analyst Workflow: The "Data-Driven Intervention"

SQL isn't just about code; it's about solving problems.

1. **Ask:** Define the specific group needed (e.g., "Full-time employees with salary $\le$ 30,000").
    
2. **Process:** Use `WHERE` clauses to filter out the noise (e.g., excluding interns).
    
3. **Share:** Use **Aliases** to rename raw database fields into human-readable labels for your manager.
    
4. **Act:** Use the clean data to make business recommendations (e.g., identifying salary inequities).
    

### 💡 Quick Reference: Your SQL Cheat Sheet

- **Filter pattern:** `WHERE column LIKE 'Value%'`
    
- **Filter exclusion:** `WHERE column <> 'Value'`
    
- **Adding notes:** `-- This is a comment`
    
- **Renaming fields:** `SELECT column AS alias_name`

## Planning Data Visualization

### 1. The 3-Step Visualization Process

1. **Explore (Patterns):** Identify trends, behaviors, or correlations in your raw data (e.g., discovering that geography impacts sales).
    
2. **Plan (Strategy):** Determine what your audience needs to know. Tailor the visual to the decision they need to make.
    
3. **Create (Execution):** Iterate. Try different formats until the story is clear. Don't be afraid to experiment with different chart types.
    

### 2. Choosing the Right Visual

Use this as a quick reference when planning your reports:

|**Visual Type**|**Best Used For**|
|---|---|
|**Line Charts**|Tracking trends or changes **over time**.|
|**Maps**|Connecting data to **geographic locations**.|
|**Donut Charts**|Showing parts-to-a-whole / **Customer segments**.|
|**Bar Charts**|Comparing quantities across different categories (e.g., total visitors).|

### 3. The Visualization Toolkit

- **Spreadsheets (Excel/Sheets):** Best for quick, simple visualizations and initial exploration.
    
- **Tableau:** A powerful, specialized tool for creating **interactive dashboards**. Use this when you need stakeholders to "click and explore" the data.
    
- **Programming (Python/R):**
    
    - **Python:** Uses **Libraries** (collections of pre-written code).
        
        - _Matplotlib:_ Flexible, foundation for static/interactive plots.
            
        - _Seaborn:_ Creates professional, polished statistical graphics easily.
            
        - _Plotly:_ Best for interactive web-based graphs.
            
    - **R/RStudio (Posit):** A professional-grade environment for high-level data visualization and analysis.
        

### 💡 Analyst Best Practice: The "Storyteller" Mindset

- **Don't force the data:** If your analysis shows a trend, choose the visual that makes that trend _obvious_ to a non-technical manager.
    
- **Tool Agnostic:** You don't need to know every tool at once. Focus on understanding the **principles** of why a chart works. If you understand the goal, you can learn the software later.