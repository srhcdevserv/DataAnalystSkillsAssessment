# Data Analyst Skills Assessment

## Overview
This assessment evaluates your ability to work with real-world healthcare-style data across two layers:

- **Data Repository (DR):** raw, transactional data  
- **Data Mart (DM):** curated, reporting-focused data  

You will be expected to:
- Write SQL queries against both layers
- Identify data quality and modeling issues
- Reconcile differences between systems
- Communicate insights clearly (SQL + dashboard)

> This assessment is designed to reflect real-world conditions. Not all data will align perfectly.

---

## Time Expectation
**Estimated time:** 1–2 hours

You are not required to complete every question. Focus on demonstrating:
- Clear reasoning
- Sound SQL practices
- Thoughtful interpretation of results

---

## Tools Allowed
You may use:
- SQL Server Management Studio (SSMS)
- Tableau Public (preferred) or Excel
- Standard documentation (e.g., syntax reference)

**Do not use AI tools to generate answers.** Submissions are expected to reflect your own work.

---

## Environment Setup

1. Install SQL Server Express or use LocalDB (included with SSMS)
2. Open SQL Server Management Studio (SSMS)
3. Connect to your local instance:
   - `(localdb)\MSSQLLocalDB`  
   - OR `.\SQLEXPRESS`

4. Open a new query window

5. Run the provided SQL scripts **in the following order**:
    - 01-CreateAssessmentDB.Database.sql
    - 02-dbo.dim_facility.Table.sql
    - 03-dbo.dim_patient.Table.sql
    - 04-dbo.dim_procedure.Table.sql
    - 05-dbo.dim_surgeon.Table.sql
    - 06-dbo.dr_patients.Table.sql
    - 07-dbo.dr_encounter.Table.sql
    - 08-dbo.dr_charges.Table.sql
    - 09-dbo.dr_payments.Table.sql
    - 10-dbo.dr_adjustments.Table.sql
    - 11-dbo.dr_clinic_lookup.Table.sql
    - 12-dbo.vw_dr_financial_summary.View.sql
    - 13-dbo.vw_dr_charges.View.sql
    - 14-dbo.fact_surgery_case.Table.sql
  
6. Confirm all tables and views are created successfully before proceeding

---

## Important Constraints

- **Do NOT modify table structures, schemas, or data**
- Do NOT add, remove, or alter columns, tables, or relationships
- All analysis must be performed using queries and/or visualization tools only

> This environment is intentionally designed with imperfections.  
> Your task is to analyze and interpret the data as provided—not to "fix" it.

---

## Data Overview

### Data Repository (DR)
- Transactional-level data (encounters, charges, payments, adjustments)
- Reflects operational system structure
- May include inconsistencies or edge cases

### Data Mart (DM)
- Aggregated, reporting-oriented data
- Structured around surgical cases and dimensions
- Does not perfectly align with DR by design

---

## Assessment Questions

### Q1. DR Financial Summary
Using DR tables, produce a summary including:
- Total Charges  
- Total Payments  
- Total Adjustments  
- Net Revenue  

Group results at a meaningful level (e.g., facility and/or month).

---

### Q2. Collection Performance
- Identify the facility with the highest collection rate  
- Highlight any anomalies or unexpected patterns  

Provide a brief explanation of your findings.

---

### Q3. Encounter Patterns
Identify patients with multiple encounters within a short time frame (e.g., 14 days).

- Describe your logic  
- Return representative results  

---

### Q4. Data Mart Analysis
Using the Data Mart:
- Analyze surgical performance by surgeon and/or procedure  
- Include at least one calculated metric (e.g., margin, average duration, case volume)

---

### Q5. Join Logic and Data Quality
Demonstrate how join strategy impacts results:

- Provide an example of an incorrect or misleading aggregation  
- Provide a corrected version  
- Explain the difference in outcomes  

---

### Q6. Cross-System Revenue Reconciliation
Compare revenue between DR and Data Mart:

- Do totals match?  
- If not, explain why  
- Identify structural drivers (e.g., grain differences, aggregation logic, transformations)  
- Attempt a reasonable reconciliation approach  

Clearly state your assumptions.

---

### Q7. Calculated Fields
Create at least one calculated field used in your analysis or dashboard.

Examples:
- Net Revenue  
- Collection Rate  
- Profit Margin  

---

## Dashboard Requirement

Create a simple dashboard (Tableau Public preferred) that includes:

- Key financial metrics  
- At least one dimensional breakdown (facility, surgeon, or procedure)  
- At least one calculated field  
- Clear labeling and organization  

---

## Submission Requirements

Submit the following:

1. **SQL File(s)**
- Queries used to answer the questions  

2. **Dashboard**
- Tableau Public link OR exported file  

3. **Summary (1–2 paragraphs or 5–10 minute screen recording explaining your approach)**
- Key findings  
- Notable data issues  
- Assumptions made  

4. **Delivery**
- Completed packages can be delivered to SRHC through recruiter contacts.
---

## Evaluation Criteria

Submissions will be evaluated based on:

- SQL accuracy and structure  
- Understanding of data modeling and joins  
- Ability to work across DR and DM layers  
- Problem-solving and reasoning  
- Clarity of communication  
- Dashboard usability and design  

---

## Feedback (Optional)

After completing the assessment, you may provide feedback on:

- Time required  
- Difficulty level  
- Clarity of instructions  

---

## Notes

- Data inconsistencies are intentional  
- Focus on reasoning, not perfect alignment  
- Clearly explain any assumptions you make  

---

**We are most interested in how you think through problems, not just final outputs.**
