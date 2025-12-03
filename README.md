 # **Automated Data Engineering & Analytics Pipeline**

## **Tagline**
A fully automated reporting workflow that transforms raw marketing CSV files into analytics-rich PowerPoint decks—complete with KPIs, visual charts, and executive-style insights.

## **1. Problem Context**
Modern marketing and AdTech teams rely heavily on data-driven reporting.
But the current process often looks like this:
- Download CSV files manually  
- Clean data in Excel  
- Create charts one by one  
- Prepare weekly slides manually  
- Repeat every week, every month, for every campaign  
This consumes hours of repetitive effort, delays insights, and introduces human error.
## **The Gap**
Teams need a way to automatically:
- Ingest raw CSVs  
- Clean and validate data  
- Compute important KPIs  
- Generate visuals  
- Produce client-ready presentations  

**2. The Solution: AutoAdDeck**
AutoAdDeck is a lightweight but powerful **ETL + reporting engine** built for analysts.  
Drop a CSV into your project and the system automatically:
- Cleans the data  
- Computes campaign-level metrics  
- Builds performance charts  
- Writes an AI-style narrative (template-based)  
- Generates a polished PPTX deck  

 **3. What You Get (Expected Output)**
After running the pipeline, AutoAdDeck produces:
**KPI Summary**
- Total impressions  
- Total clicks  
- Total spend & revenue  
- Avg. CTR, CPC, ROAS  
- Best & worst campaigns  
**Visual Analytics**
- Bar chart comparing impressions, clicks, and revenue across campaigns  
**Executive Narrative**
- A concise, human-readable summary explaining overall performance  

 **4. Architecture & Workflow**
The system follows a clean and modular **Data Engineering workflow**:
**1. Ingestion**
Reads raw CSV data using Pandas with validation for required columns
**2. Transformation**
Data is cleaned, converted, and enriched with derived KPIs:
- CTR  
- CPC  
- CPA  
- ROAS
 **3. Analytics Layer**
- Aggregates metrics across campaigns  
- Identifies highest- and lowest-performing campaigns  
 **4. Visualization**
Generates campaign performance charts using Matplotlib.

**5. Tech Stack**
| **Component**       | **Technology**               |
|---------------------|------------------------------|
| Language            | Python 3.10+                 |
| Data Processing     | Pandas                       |
| Visualization       | Matplotlib                   |
| Reporting           | python-pptx                  |
| File Handling       | argparse, pathlib            |
| Extras              | Template-based narrative generator |


**6. Key Challenges & Learnings**

**1. Handling Missing or Partial Data**
Marketing datasets often contain inconsistent or incomplete fields.  
To ensure pipeline stability:
- Missing columns (e.g., *conversions*, *revenue*) are auto-created  
- Zero values are safely replaced to avoid division errors  
- Schema validation prevents runtime failures  
**2. Building a Modular ETL Structure**
Instead of writing everything inside one script, the pipeline follows a clean modular workflow:
load → preprocess → analyze → visualize → generate deck
This approach:
- Improves readability  
- Makes debugging easier  
- Allows the project to scale  
- Makes it production-ready and extensible for future enhancements  

**7.Conclusion**
AutoAdDeck eliminates repetitive manual work from analytics and reporting workflows. 
It functions as a mini data engineering pipeline,analytics engine,and automated slide generato—all in one system.
By automating data ingestion, cleaning, KPI computation, charting, and report generation, AutoAdDeck enables marketers and analysts to focus on insights and decision-making, not on formatting slides.


