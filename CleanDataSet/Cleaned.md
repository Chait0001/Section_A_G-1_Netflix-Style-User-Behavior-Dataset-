## Dataset Description

**Source:** `Raw_Dataset.csv`
**Initial Sample:** 10,000 rows
**Final Cleaned Dataset:** ~6,685 rows

---

## Data Cleaning & Preparation

The dataset was cleaned and transformed to ensure consistency, reliability, and suitability for business insights related to **user engagement and subscription revenue optimization**.

---

### Handling Missing Values

Missing values were treated carefully to maintain dataset size and distribution.

| Column              | Missing Values | Treatment                |
| ------------------- | -------------- | ------------------------ |
| gender              | 823            | Mode imputation (Female) |
| household_size      | 1514           | Median imputation (2)    |
| progress_percentage | —              | Median imputation        |
| age                 | —              | Median imputation        |

Rows were **not deleted** to preserve dataset size and distribution.

---

### Age Filtering

Invalid or unrealistic age values were filtered to ensure meaningful demographic insights.

---

### Removing Invalid Values

Records with incorrect or inconsistent entries were removed to improve data quality.

---

### Duplicate Handling

Duplicate records were identified and removed to prevent repeated viewing activity from biasing analysis.

---

### Text Standardization

Categorical columns were standardized by:

* Removing extra spaces
* Fixing letter case
* Normalizing country names (e.g., USA)

**Affected Columns:**

* subscription_plan
* device_type
* country
* content_type
* genre_primary

---

### Boolean Standardization

The following columns were standardized to consistent TRUE/FALSE values:

* is_active
* is_netflix_original

This ensured consistency in filtering and aggregation.

---

### Rating Transformation

The original rating column contained certification labels.
A new column **maturity_level** was created for better audience segmentation.

| Rating          | Maturity Level |
| --------------- | -------------- |
| G, TV-Y, TV-Y7  | Kids           |
| PG, TV-PG       | Family         |
| PG-13, TV-14    | Teens          |
| R, TV-MA, NC-17 | Adult          |

This improves visualization clarity and segmentation analysis.

---

### Data Type Formatting

Columns were converted to appropriate formats:

* **Date:** watch_date
* **Numeric:** duration, progress, age, spend, household_size, imdb_rating
* **Categorical:** device, genre, country, language, etc.

---

## 🗑️ Column Removal with Justification

The following columns were removed because they did not support engagement or revenue optimization goals.

---

### 1. user_rating

**Why deleted:**

* Contains 8082 null values (very high missing data).
* The analysis focuses on engagement and revenue, not user review behavior.
* IMDb rating already represents content quality.

**Decision:** Removed due to high nulls and redundancy.

---

### 2. genre_secondary

**Why deleted:**

* 6494 null values.
* Adds complexity with minimal additional insight.
* Primary genre is sufficient for performance analysis.

**Decision:** Removed to simplify analysis.

---

### 3. production_budget

**Why deleted:**

* 6410 null values.
* Relevant to studio financial performance, not streaming engagement.

**Decision:** Removed as it does not support engagement or revenue optimization.

---

### 4. box_office_revenue

**Why deleted:**

* 6746 null values.
* Streaming platforms generate revenue through subscriptions, not box office.

**Decision:** Removed due to irrelevance to the business model.

---

### 5. number_of_seasons

**Why deleted:**

* 7272 null values.
* Applicable only to TV shows.

**Decision:** Removed to maintain consistency.

---

### 6. number_of_episodes

**Why deleted:**

* 6971 null values.
* Relevant only for series.

**Decision:** Removed to maintain dataset consistency.

---

## Additional Columns Removed

These columns did not support engagement or revenue insights:

* session_id → too granular
* user_id → personal identifier
* movie_id → technical ID
* email → personal data
* first_name → personal data
* last_name → personal data
* state_province → too detailed
* city → too granular
* created_at → technical timestamp
* location_country → duplicate of country
* primary_device → duplicate of device_type

---

## Final Dataset Structure

After preprocessing:

* The dataset contains **6,685 rows**
* No critical missing values remain
* All columns are standardized and formatted

