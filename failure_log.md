# Failure Log

## Test 1
- Document: Internship offer letter (Ezitech Software House)
- Fields tested: intern_name, intern_id, position, joining_date, ending_date, company_name, contact_person, contact_number
- Output: Valid JSON, all fields correctly extracted
- Failure: None — worked on first try
- Prompt change: None needed

## Test 2
- Document: Invoice (INV-178912471692)
- Fields tested: same schema as Test 1
- Output: Valid JSON, correctly returned null for fields not present (intern_id, position, joining_date, ending_date)
- Failure: None — schema mismatch handled correctly, no hallucinated values
- Prompt change: None needed
