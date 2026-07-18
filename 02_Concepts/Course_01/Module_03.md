---
date: 2026-07-18
Parent: "[[Module_03-Lecture Notes]]"
---

### 1. Data Structuring and Preparation

The foundation of any analysis is having data that is organized and reliable.

- **The Spreadsheet Structure:** Spreadsheets rely on a clean structure where headers (labels) clearly define the attributes in the data, and cells store the specific values.
    
- **Processing for Accuracy:** Before analysis can begin, data must be formatted and sorted. A key procedural rule here is to always verify "Data has header row" when sorting, otherwise, you risk reordering your labels along with your data, which ruins the dataset.
    

### 2. The SQL Logic and Problem-Solving Workflow

SQL is not just a coding language; it is a tool for filtering "noise" to find answers.

- **The Problem-Solving Workflow:**
    
    - **Ask:** Define the specific business group or problem you are investigating.
        
    - **Process:** Use SQL `WHERE` clauses to filter out irrelevant data (like excluding interns) so you focus only on the relevant group.
        
    - **Share/Act:** Use `Aliases` (AS) to translate raw, technical database field names into human-readable labels so that managers and stakeholders can easily understand your recommendations.
        
- **Code Maintenance:** SQL is intended to be read by teammates. Using uppercase for commands, proper indentation, terminators (;), and clear comments (-- or /* */) ensures your logic is understandable to others and your future self.
    

### 3. Strategic Data Visualization

Visualization is the bridge between raw data and business action.

- **The Storyteller Mindset:** Effective visualization is "tool agnostic." The goal is not to master every software feature, but to understand the principles of why a chart works. If your analysis shows a clear trend, your job is to choose the visual format that makes that trend undeniable to a non-technical audience.
    
- **Planning vs. Execution:** Do not jump straight into building charts. First, explore the patterns, then plan your strategy based on what the audience needs to decide, and only then execute by iterating on your visuals.
    
- **Selection Logic:**
    
    - **Trends:** Use line charts.
        
    - **Geography:** Use maps.
        
    - **Parts-to-Whole:** Use donut charts.
        
    - **Comparisons:** Use bar charts.