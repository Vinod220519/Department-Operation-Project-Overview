#📦 Department-Operation-Project-Overview
Platform:** Microsoft Fabric + Power BI   

##📝 Project Summary
This project provides an operational overview of each department by combining employee, project, and budget data in Microsoft Fabric, building SQL views and a semantic model, and creating an interactive Power BI dashboard (`Project Overview Department Operation`).   

##📑 Files in this repository
  - `data/`  
  - `completed_projects.csv`  
  - `departments.csv`  
  - `employees.csv`  
  - `project_assignments.csv`  
  - `projects.csv`  
  - `upcoming projects.csv`  
  - `headshots'

- `fabric/`  
  - `sql_views/department_view.sql`  — SQL used to build the `department` view  
  - `sql_views/cost_view.sql`        — SQL used to build the `cost` view
- `semantic_model/`  
  - `model.json` or exported semantic model files
- `powerbi/`  
  - `Project_Overview_Department_Operation.pbix` (Power BI Desktop file)
- `docs/`  
  - `Project Report.docx`  — full project report (attached)
 
  ##📌 Data Processing & Architecture
1. CSV files uploaded to a Lakehouse in Microsoft Fabric (OneLake).  
2. Dataflow Gen2 cleans and standardizes source files.  
3. SQL views (`department`, `cost`) in Warehouse combine and aggregate the data (CTE used for `project_status`).  
4. Semantic model exposes `department`, `cost`, and `Head_Shots` to Power BI.  
5. Power BI connects to the semantic model for reporting.  
6. A pipeline triggers Dataflow Gen2 and semantic model refresh on schedule.

##📌 Key Visuals & KPIs
- - Donut charts: project distribution (by status & department)
- - KPI cards: Total Capital, Project Budget
- - Employee profile card with headshot and attributes
- - Department table: goals, project cost, salary cost, budget, capital
- - Bar charts: project budget by department, project-level budget

  /department-operation/  
├─ data/   
│  ├─ completed_projects.csv   
│  ├─ departments.csv   
│  ├─ employees.csv   
│  ├─ project_assignments.csv    
│  ├─ projects.csv    
│  ├─ upcoming projects.csv    
│  └─ headshots/    
├─ fabric/  
│  └─ sql_views/   
│     ├─ department_view.sql   
│     └─ cost_view.sql   
├─ semantic_model/   
│  └─ model_export_files...    
├─ powerbi/   
│  └─ Project_Overview_Department_Operation.pbix   
├─ docs/   
│  ├─ Project Report.docx   
│  └─ BRD.md   


Live Dashboard link :  https://app.powerbi.com/reportEmbed?reportId=6b616250-7c1f-4d2c-b617-44ea2b609112&autoAuth=true&ctid=16a0c667-b584-40e4-a440-9e56f4a337ee


