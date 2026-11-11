# Capstone Project 4 | START HERE

## Recommended order
1. Download and IMPORT `06_n8n_Vendor_Comparison_Importable_Workflow.json` into a blank n8n workflow (canvas three-dot menu > Import from File).
2. Read `08_n8n_End_to_End_Step_by_Step_Guide.pdf` (or the editable `.docx` version).
3. In n8n, click **Execute Workflow** and submit the Procurement Intake Form using reviewer `Demo Procurement Officer` and PR `PR-NOVA-001`.
4. The results should show **Vendor B / BluePeak Devices**, **INR 140,420**, weighted score **97.32/100**.
5. Leave Vendor B selected and choose **Approve selected vendor (SIMULATION)**; review the execution's `auditRecord`.
6. Test a human override selecting Vendor C with a reason of at least 10 characters; then test a rejection.
7. Optional: follow guide section 9 to create an n8n Data Table and insert durable demo audit rows.

### Tool limitations
- Base project runs with n8n Form/Code nodes: external API key required.
- ChatGPT Pro/Gemini Pro can help extract data from the supplied fictional PDFs *manually*. Neither chat plan automatically gives n8n model API access.
- In this starter workflow the three PDF contents are already represented as demo data in the `Load Sample Quotes and Policy` Code node. The PDFs are NOT automatically ingested by n8n.
- `03_Approval_History.csv` is a template, not updated automatically. Without Data Table extension, audit records exist in execution output/history subject to instance retention.
- No real emails, PO, SAP posting, payment or vendor commitment.

### Project files
`01_Requirements.csv`, 
`02_Standardized_Quotes.csv`, 
`03_ Procurement_Policy.md`, 
`04_AI_Quotation_Extraction_Prompt.txt`, 
`05_Vendor Comparison and Procurement Assistant `, 
`06_ n8n_End_to_End_Step_by_Step_Guide.docx`, 
`Quotation_A/B/C_*.pdf`.

All organizations, quotes, ratings and policies in this package are fictional.

