# Vendor Comparison and Procurement Assistant

A demo n8n workflow for comparing vendor quotations, applying procurement policies, recording approvals, and testing human overrides.

## Recommended order

1. Download and import `06_n8n_Vendor_Comparison_Importable_Workflow.json` into a blank n8n workflow:
   **Canvas menu (⋯) → Import from File**.
2. Read `08_n8n_End_to_End_Step_by_Step_Guide.pdf` or the editable `.docx` version.
3. In n8n, select **Execute Workflow** and submit the Procurement Intake Form with:
   - **Reviewer:** `Demo Procurement Officer`
   - **PR:** `PR-NOVA-001`
4. Confirm that the results show:

   | Result | Expected value |
   | --- | --- |
   | Selected vendor | Vendor B / BluePeak Devices |
   | Total | INR 140,420 |
   | Weighted score | 97.32/100 |

5. Leave Vendor B selected and choose **Approve selected vendor (SIMULATION)**. Review the execution's `auditRecord`.
6. Test a human override by selecting Vendor C and entering a reason of at least 10 characters. Then test a rejection.
7. Optional: follow section 9 of the guide to create an n8n Data Table and insert durable demo audit rows.

## Tool limitations

> [!IMPORTANT]
> - The base project uses n8n Form and Code nodes. An external API key is required for external API features.
> - ChatGPT Pro or Gemini Pro can help extract data from the supplied fictional PDFs manually. Neither plan automatically provides n8n model API access.
> - In this starter workflow, the three PDF contents are already represented as demo data in the **Load Sample Quotes and Policy Code** node. The PDFs are **not** automatically ingested by n8n.
> - `03_Approval_History.csv` is a template and is not updated automatically. Without the Data Table extension, audit records remain in execution output/history subject to instance retention.
> - This project does not send real emails, create purchase orders, post to SAP, process payments, or commit vendors.

## Project files

- `01_Requirements.csv`
- `02_Standardized_Quotes.csv`
- `03_Procurement_Policy.md`
- `04_AI_Quotation_Extraction_Prompt.txt`
- `05_Vendor Comparison and Procurement Assistant`
- `06_n8n_End_to_End_Step_by_Step_Guide.docx`
- `Quotation_A/B/C_*.pdf`

## Disclaimer

All organizations, quotes, ratings, and policies in this package are fictional.