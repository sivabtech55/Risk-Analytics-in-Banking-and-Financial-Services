### Project Title:
Risk Analysis in Banking and Financial Services using Data Analytics and Visualization

### Project Objective:
To identify and evaluate key financial and customer behavior risk factors using data analytics techniques, with the goal of helping banks make data-driven decisions to minimize defaults, credit risk, and customer churn.

### Project Description:
This project involves analyzing banking data to assess potential risks associated with loans, deposits, and customer segments. It leverages data analytics tools like Python (Pandas, Seaborn, Matplotlib), SQL, and Power BI to:

Understand the distribution of loan defaults, deposit patterns, and credit card usage.

Evaluate customer risk levels based on factors such as income band, occupation, nationality, and account activity.

Develop interactive Power BI dashboards with KPIs like:

Total Clients

Total Loans / Bank Loans / Business Lending

Total Deposits / Bank Deposits

Checking and Savings Account Amounts

Total Credit Card Amount and Balance

Estimated Income Analysis

Loan Risk by Occupation and Nationality

Loyalty Classification Patterns

Using both statistical and visual methods, the project identifies high-risk customer profiles, loan performance trends, and early indicators of financial instability, supporting smarter risk management strategies for banking institutions.

## DataSet

- <a href="https://github.com/sivabtech55/Risk-Analytics-in-Banking-and-Financial-Services/blob/main/Banking.xlsx">Banking Dataset</a>


## Key Performance Indicators (KPIs) – Banking and Financial Services Project

Below are the KPIs calculated in this project using customer, loan, and deposit data. These KPIs help financial institutions monitor performance, customer behavior, and lending risk.

---

### Client & Account KPIs
| KPI | Description |
|-----|-------------|
| **Total Clients** | Total number of unique banking customers |
| **Estimated Average Income** | Average income across all clients |
| **Loyalty Classification Breakdown** | Distribution of clients by loyalty tier (e.g., Bronze, Silver, Gold) |
| **Clients by Occupation** | Grouping of clients based on their declared profession |
| **Clients by Nationality** | Segmentation of clients by country/national origin |

---

### Deposit & Account Balance KPIs
| KPI | Description | Formula / Example |
|-----|-------------|------------------|
| **Total Deposit Amount** | Combined value of all bank deposits | `SUM(bank_deposit)` |
| **Total Bank Deposit** | Amount held in term or time deposits only | `SUM(bank_deposit WHERE type = 'term')` |
| **Total Checking Account Amount** | Combined value in all checking/current accounts | `SUM(checking_account_amount)` |
| **Total Savings Account Amount** | Combined value in all savings accounts | `SUM(savings_account_amount)` |
| **Average Deposit per Client** | Measures financial activity | `Total Deposit / Total Clients` |

---

### 🏦 Lending KPIs
| KPI | Description |
|-----|-------------|
| **Total Loan Amount** | Total of all loans issued (personal, auto, home, etc.) |
| **Total Bank Loan** | Total of loans issued directly by the bank |
| **Total Business Lending** | Amount lent to businesses (SMEs or corporate) |
| **Bank Loan by Nationality** | Breakdown of loan value by customer nationality |
| **Bank Loan by Occupation** | Breakdown of loan amount based on client occupation |
| **Average Loan per Customer** | Helps assess average debt level per client |

---

### Credit Card KPIs
| KPI | Description |
|-----|-------------|
| **Total Credit Card Amount Issued** | Total value limit across all credit cards |
| **Total Credit Card Balance** | Total outstanding credit card balance |
| **Average Utilization Rate** | `(Credit Card Balance / Credit Card Limit) × 100` |

---

## Sample KPI SQL Queries

```sql
-- Total Clients
SELECT COUNT(DISTINCT client_id) AS total_clients FROM customer_data;

-- Total Deposit
SELECT SUM(bank_deposit) AS total_deposit FROM account_data;

-- Bank Loan by Nationality
SELECT nationality, SUM(bank_loan) AS total_loan
FROM loan_data
GROUP BY nationality;

-- Credit Card Balance
SELECT SUM(credit_card_balance) AS total_credit_card_balance FROM credit_data;
