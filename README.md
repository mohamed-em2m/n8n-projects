# n8n-projects
video link :https://www.veed.io/view/b6ccc118-3686-461d-8329-3dff015fd5eb?source=editor&panel=share
workflow link n8n : https://emam2002.app.n8n.cloud/workflow/XCeJ7LnIN4BfUww4 
This workflow implements a scheduled data processing pipeline that fetches user and post data from external APIs, enriches and transforms it, then routes results to different endpoints based on business logic. The architecture uses parallel data fetching (users and posts simultaneously), followed by deduplication, merging on userId, and extraction of key fields including calculated company sizes. Data then flows through three parallel branches: domain filtering (example.com), company size-based routing (VIP vs regular users), and aggregation reporting with conditional warning notifications.
<img width="1179" height="724" alt="Screenshot From 2025-12-23 18-08-02" src="https://github.com/user-attachments/assets/7f6896d4-6d4c-4fe8-97da-c01be9000350" />
