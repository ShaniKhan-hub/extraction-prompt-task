# Extraction Prompt v1

Extract the following fields from the document text below and return ONLY valid JSON, no extra text, no markdown formatting:

{
  "intern_name": "",
  "intern_id": "",
  "position": "",
  "joining_date": "",
  "ending_date": "",
  "company_name": "",
  "contact_person": "",
  "contact_number": ""
}

If a field is not present in the document, use null.

Document text:
"""
[PASTE DOCUMENT TEXT HERE]
"""
