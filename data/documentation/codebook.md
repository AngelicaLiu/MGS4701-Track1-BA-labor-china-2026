# Codebook

## Fields
- `record_id`: Unique identifier (e.g., A001, B001).
- `collector`: Initial of the collector.
- `collection_date`: Date of collection (YYYY/MM/DD).
- `job_title_raw`: Original job title.
- `job_title_standardized`: Cleaned job title.
- `role_family`: Business Analyst / Data Analyst / BI Analyst / Operations Analyst / Data Science / Data Product/BP / Other.
- `eligible`: 1 if the posting is a valid BA/DA role, 0 otherwise.
- `salary_min_clean` / `salary_max_clean`: Parsed monthly salary in RMB.
- `salary_period`: month / day.
- `ai_flag`: 1 if JD mentions AI-related keywords (LLM, ChatGPT, AIGC, 大模型, etc.), 0 otherwise.
- `sql_flag`: 1 if JD mentions SQL, 0 otherwise.
- `python_flag`: 1 if JD mentions Python, 0 otherwise.

## Missing Values
Missing values are coded as `NA` or left blank. They are not imputed.