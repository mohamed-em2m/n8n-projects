# n8n Projects - Data Processing Workflow

**Video Demo:** [Watch here]([https://drive.google.com/file/d/15J7XXR3vwpYjw5UVt9flz_AcTKI7vPkJ/view?usp=sharing])
**n8n Workflow Link:** [Open workflow](https://emam2002.app.n8n.cloud/workflow/XCeJ7LnIN4BfUww4)  

---

## Overview

This workflow implements a **scheduled data processing pipeline** that:

- Fetches **user and post data** from external APIs simultaneously.
- Enriches and transforms the data.
- Routes results to **different endpoints** based on business logic.

The architecture includes:

- **Parallel Data Fetching:** Users and posts are fetched concurrently.
- **Data Deduplication & Merging:** Users and posts are merged on `userId`.
- **Field Extraction & Enrichment:** Key fields are extracted, including full name, email, phone, company name, processed timestamp, and calculated company sizes.

---

## Workflow Branches

After transformation, the data flows through **three parallel branches**:

1. **Domain Filtering**  
   - Filters users whose email domain is `example.com`.
2. **Company Size-Based Routing**  
   - Routes users to **VIP** or **regular** endpoints based on company size.
3. **Aggregation & Reporting**  
   - Generates summary reports.
   - Conditional warning notifications for data anomalies.

---

## Screenshot

<img width="1179" height="724" alt="Workflow Screenshot" src="https://github.com/user-attachments/assets/7f6896d4-6d4c-4fe8-97da-c01be9000350" />


## How to Test / Run

1. Import the workflow via the [n8n workflow link](https://emam2002.app.n8n.cloud/workflow/XCeJ7LnIN4BfUww4).  
2. Set up any required credentials or webhooks (e.g., `webhook.site` or Google Sheets).  
3. Execute manually or let the schedule trigger run the workflow.  
4. Observe outputs in the configured destinations and notifications.

---

## Notes

- The workflow demonstrates **concurrent branches, error handling, and aggregation**.
- Designed to be modular: new branches or conditions can be added without disrupting existing logic.
